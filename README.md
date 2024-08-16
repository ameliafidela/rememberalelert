# rememberalelert
ini untuk extention kodular 
chrome.alarms.create("myAlarm", { delayInMinutes: 1 });

chrome.alarms.onAlarm.addListener((alarm) => {
  if (alarm.name === "myAlarm") {
    chrome.notifications.create({
      type: "basic",
      iconUrl: "icon.png",
      title: "Alarm",
      message: "Waktunya alarm!"
    });
  }
});
