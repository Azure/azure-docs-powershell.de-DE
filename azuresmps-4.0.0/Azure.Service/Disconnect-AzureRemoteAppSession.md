---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005892"
---
# <span data-ttu-id="14c7a-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="14c7a-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="14c7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="14c7a-103">Trennt eine Azure RemoteApp-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="14c7a-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="14c7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14c7a-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="14c7a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="14c7a-106">Das Cmdlet " **trennen-AzureRemoteAppSession** " trennt die Verbindung zwischen der Azure RemoteApp-Sitzung eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="14c7a-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="14c7a-107">Der Client des Benutzers trennt die Verbindung zu seiner Azure RemoteApp-Sitzung, aber die Programme des Benutzers werden weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14c7a-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="14c7a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14c7a-108">EXAMPLES</span></span>

### <span data-ttu-id="14c7a-109">Beispiel 1: Trennen der Sitzung eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="14c7a-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="14c7a-110">Dieser Befehl trennt die Azure RemoteApp-Sitzung in der ContosoApps-Sammlung für den Benutzer, dessen UPN lautet PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="14c7a-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="14c7a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="14c7a-111">PARAMETERS</span></span>

### <span data-ttu-id="14c7a-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="14c7a-112">-CollectionName</span></span>
<span data-ttu-id="14c7a-113">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="14c7a-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="14c7a-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="14c7a-114">-Profile</span></span>
<span data-ttu-id="14c7a-115">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="14c7a-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14c7a-116">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="14c7a-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14c7a-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="14c7a-117">-UserUpn</span></span>
<span data-ttu-id="14c7a-118">Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers an, beispielsweise PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="14c7a-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="14c7a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c7a-119">CommonParameters</span></span>
<span data-ttu-id="14c7a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c7a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c7a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c7a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c7a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14c7a-122">INPUTS</span></span>

## <span data-ttu-id="14c7a-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14c7a-123">OUTPUTS</span></span>

## <span data-ttu-id="14c7a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="14c7a-124">NOTES</span></span>

## <span data-ttu-id="14c7a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14c7a-125">RELATED LINKS</span></span>

[<span data-ttu-id="14c7a-126">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="14c7a-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="14c7a-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="14c7a-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="14c7a-128">Senden-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="14c7a-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


