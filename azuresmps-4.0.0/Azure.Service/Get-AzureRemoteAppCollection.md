---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006535"
---
# <span data-ttu-id="25bdd-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="25bdd-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="25bdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="25bdd-103">Ruft Informationen zu einer Azure RemoteApp-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="25bdd-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="25bdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25bdd-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="25bdd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="25bdd-106">Das Cmdlet " **Get-AzureRemoteAppCollection** " Ruft Informationen zu Azure RemoteApp-Auflistungen in Microsoft Azure ab.</span><span class="sxs-lookup"><span data-stu-id="25bdd-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="25bdd-107">Sie gibt ein Objekt zurück, das Informationen zu einer bestimmten Sammlung enthält, oder wenn für alle Auflistungen im aktuellen Abonnement keine Sammlung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="25bdd-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="25bdd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25bdd-108">EXAMPLES</span></span>

### <span data-ttu-id="25bdd-109">Beispiel 1: Abrufen einer Liste aller Auflistungen</span><span class="sxs-lookup"><span data-stu-id="25bdd-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="25bdd-110">Dieser Befehl gibt eine Liste aller Azure RemoteApp-Auflistungen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="25bdd-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="25bdd-111">Beispiel 2: Abrufen von Informationen zu einer angegebenen Sammlung</span><span class="sxs-lookup"><span data-stu-id="25bdd-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="25bdd-112">Dieser Befehl gibt Informationen zur Azure RemoteApp-Sammlung mit dem Namen "ContosoApps" zurück.</span><span class="sxs-lookup"><span data-stu-id="25bdd-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="25bdd-113">Beispiel 3: Abrufen einer Liste von Auflistungen mit einem Platzhalter</span><span class="sxs-lookup"><span data-stu-id="25bdd-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="25bdd-114">Dieser Befehl gibt eine Liste aller Azure RemoteApp-Auflistungen zurück, die auf Finance \* abgestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="25bdd-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="25bdd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="25bdd-115">PARAMETERS</span></span>

### <span data-ttu-id="25bdd-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="25bdd-116">-CollectionName</span></span>
<span data-ttu-id="25bdd-117">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="25bdd-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="25bdd-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="25bdd-118">-Profile</span></span>
<span data-ttu-id="25bdd-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="25bdd-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25bdd-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="25bdd-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25bdd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bdd-121">CommonParameters</span></span>
<span data-ttu-id="25bdd-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25bdd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bdd-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25bdd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bdd-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25bdd-124">INPUTS</span></span>

## <span data-ttu-id="25bdd-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25bdd-125">OUTPUTS</span></span>

## <span data-ttu-id="25bdd-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="25bdd-126">NOTES</span></span>

## <span data-ttu-id="25bdd-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25bdd-127">RELATED LINKS</span></span>

[<span data-ttu-id="25bdd-128">Neu – AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="25bdd-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="25bdd-129">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="25bdd-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="25bdd-130">Satz-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="25bdd-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="25bdd-131">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="25bdd-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


