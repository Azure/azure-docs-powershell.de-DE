---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006639"
---
# <span data-ttu-id="d6358-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="d6358-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="d6358-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6358-102">SYNOPSIS</span></span>
<span data-ttu-id="d6358-103">Sendet eine Nachricht an einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d6358-103">Sends a message to a user.</span></span>

## <span data-ttu-id="d6358-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6358-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d6358-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6358-105">DESCRIPTION</span></span>
<span data-ttu-id="d6358-106">Das Cmdlet " **Send-AzureRemoteAppSessionMessage** " sendet eine Nachricht an einen Benutzer, der mit einer Azure RemoteApp-Sitzung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d6358-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="d6358-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6358-107">EXAMPLES</span></span>

### <span data-ttu-id="d6358-108">Beispiel 1: Senden einer Nachricht an einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="d6358-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="d6358-109">Mit diesem Befehl wird eine Nachricht an den Benutzer gesendet, dessen UPN lautet PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="d6358-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="d6358-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6358-110">PARAMETERS</span></span>

### <span data-ttu-id="d6358-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d6358-111">-CollectionName</span></span>
<span data-ttu-id="d6358-112">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="d6358-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6358-113">-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d6358-113">-Message</span></span>
<span data-ttu-id="d6358-114">Gibt die Nachricht an, die gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6358-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6358-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="d6358-115">-Profile</span></span>
<span data-ttu-id="d6358-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d6358-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6358-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d6358-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6358-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="d6358-118">-UserUpn</span></span>
<span data-ttu-id="d6358-119">Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers an, beispielsweise PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="d6358-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6358-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6358-120">CommonParameters</span></span>
<span data-ttu-id="d6358-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6358-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6358-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6358-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6358-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6358-123">INPUTS</span></span>

## <span data-ttu-id="d6358-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6358-124">OUTPUTS</span></span>

## <span data-ttu-id="d6358-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6358-125">NOTES</span></span>

## <span data-ttu-id="d6358-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6358-126">RELATED LINKS</span></span>

[<span data-ttu-id="d6358-127">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="d6358-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="d6358-128">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="d6358-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="d6358-129">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="d6358-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


