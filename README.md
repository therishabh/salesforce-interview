# Salesforce Interview

**Q. wht is view state?**
Ans: View state is a state of you VF page, which help salesforce to regenerate VF page when it come back from server
For exmaple, when you create a VF page having a some input fields, no consider that you load this page with some value and there are some required field on this page and when you click on a button this page will get submited to server then when server replay back your page should be loaded in same state as it was before submit button click, to mantain this salesforce exchange data between VF and saevers and this information which salesforce mantian is know as View state,
In simple words , it is a state ot view which you are view and salesforce use it to regenerate your page, when ever there reply come back from server
other then transient, you can user VF remoting and @ remote action, as it wont transfer View state
