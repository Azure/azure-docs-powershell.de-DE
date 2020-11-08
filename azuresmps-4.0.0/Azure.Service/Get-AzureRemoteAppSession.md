---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006783"
---
# <span data-ttu-id="6d031-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="6d031-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="6d031-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d031-102">SYNOPSIS</span></span>
<span data-ttu-id="6d031-103">Listet alle aktiven und getrennten Azure RemoteApp-Sitzungen für eine Sammlung auf.</span><span class="sxs-lookup"><span data-stu-id="6d031-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="6d031-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d031-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d031-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d031-105">DESCRIPTION</span></span>
<span data-ttu-id="6d031-106">Das Cmdlet " **Get-AzureRemoteAppSession** " listet alle aktiven und getrennten Azure RemoteApp-Sitzungen für eine Azure RemoteApp-Sammlung auf.</span><span class="sxs-lookup"><span data-stu-id="6d031-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="6d031-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d031-107">EXAMPLES</span></span>

### <span data-ttu-id="6d031-108">Beispiel 1: Auflisten aller Sitzungen in einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="6d031-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="6d031-109">Dieser Befehl listet alle Sitzungen in der Azure RemoteApp-Sammlung mit dem Namen "ContosoApps" auf.</span><span class="sxs-lookup"><span data-stu-id="6d031-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="6d031-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d031-110">PARAMETERS</span></span>

### <span data-ttu-id="6d031-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="6d031-111">-CollectionName</span></span>
<span data-ttu-id="6d031-112">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="6d031-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="6d031-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="6d031-113">-Profile</span></span>
<span data-ttu-id="6d031-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6d031-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6d031-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6d031-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6d031-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="6d031-116">-UserUpn</span></span>
<span data-ttu-id="6d031-117">Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers an, für den Azure RemoteApp-Sitzungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d031-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="6d031-118">Der UPN kann Beispiels PattiFuller@contoso.com Weise folgendes Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="6d031-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="6d031-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d031-119">CommonParameters</span></span>
<span data-ttu-id="6d031-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d031-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d031-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d031-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d031-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d031-122">INPUTS</span></span>

## <span data-ttu-id="6d031-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d031-123">OUTPUTS</span></span>

## <span data-ttu-id="6d031-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d031-124">NOTES</span></span>

## <span data-ttu-id="6d031-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d031-125">RELATED LINKS</span></span>

[<span data-ttu-id="6d031-126">Trennen-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="6d031-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="6d031-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="6d031-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="6d031-128">Senden-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="6d031-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


