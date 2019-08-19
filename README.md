# NavPaneBug
Demo project for bug: NavigationView pane doesn't open after navigating to page with enabled cache

MainPage has NavigationView control. NavigationCacheMode of MainPage is Enabled. Button "Click me" navigates to ViewerPage. You can navigate back to MainPage from ViewerPage.

Scenario to reproduce bug:
1. Close NavigationView pane by clicking Menu button;
2. Click button "Click me";
3. Click return button in top-left corner to navigate to MainPage;
4. Open NavigationView pane by clicking Menu button.

Pane should open but sometimes pane is drawn like closed (pane is Visible but it looks like it is cutted or right panel of NavigationView with content is over it).
Property "IsPaneOpen" of NavigationView is true. Next click closes the pane, and the next one opens the pane.
If you didn't get such behavior, you can repeat steps 1-4 untill you will get it.
Problem only acuares after navigating back to MainPage. It seems that this bug is related to page's cache.
