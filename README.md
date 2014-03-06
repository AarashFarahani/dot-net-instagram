instagramdotnet
===============

C# Wrapper for Instagram Rest API

## Synopsis

instagram dot net is a class which you can use to interact with Instagram's API endpoints. It's a simple plugin that allows you to access public streams in under 5 lines of code. If you have any questions please find me on twitter @codechmst

## Code Example

    using InstagramDotNet;
  
    Instagram ig = new Instagram("YOUR_ACCESS_TOKEN");
  
    //Outputs the numeric value of a username
    //returns a JSON String containing the user id value
    getUserId("USER_NAME");
  
    //Utilize the getMediaRecent Endpoint
    //The second parameter is the number of recent images to return
    Repeater1.DataSource = ig.getMediaRecent("INSTAGRAM_USER_ID", 10);
    Repeater1.DataBind();
    
    <asp:Repeater ID="Repeater1" runat="server">
      <ItemTemplate>
          <div>
              <img src='<%# Eval("SmallImage") %>' alt='<%# Eval("Caption") %>' />
              <p><%# Eval("Tags") %></p>
              <p>&hearts; <%# Eval("Likes") %></p>
          </div>
      </ItemTemplate>
    </asp:Repeater>

## Installation

You must download and add a reference to json.net
http://james.newtonking.com/json

You can use the Instagram class as is, or compile it into a DLL for portability.

## API Reference

http://instagram.com/developer/endpoints/


## License

MIT license
