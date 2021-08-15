## CLIPBOARD IMPLEMENTATION
### PS :


This is a short project I made based on a conversation with my friend @Meghdut-Mandal. 
![Bet Image](https://github.com/vijay-gautam/c2c/blob/main/bet.png?raw=true)

sry non hindi readers.
It's basically inspired by [ihatemailto.com](https://ihatemailto.com/).


## 📣IMPORATANT STUFF 
### Implementaion : 
```javascript
    async function copyTextToClipboard(text) {
      if ('clipboard' in navigator) {
        return await navigator.clipboard.writeText(text);
      } else {
        return document.execCommand('copy', true, text);
      }
    }
  
    // onClick handler function for the copy button
    const handleCopyClick = () => {
      // Asynchronously call copyTextToClipboard
      copyTextToClipboard(copyText)
        .then(() => {
          // If successful, update the isCopied state value
          setIsCopied(true);
          setTimeout(() => {
            setIsCopied(false);
          }, 3000);
        })
        .catch((err) => {
            //handle you error accordingly
          console.log(err);
        });
    }

    //use your function
    <button onClick={handleCopyClick}>
```





