---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006776"
---
# <span data-ttu-id="57966-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="57966-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="57966-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57966-102">SYNOPSIS</span></span>
<span data-ttu-id="57966-103">Ruft Informationen zu Azure RemoteApp-virtuellen Netzwerken in Azure ab.</span><span class="sxs-lookup"><span data-stu-id="57966-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="57966-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57966-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="57966-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57966-105">DESCRIPTION</span></span>
<span data-ttu-id="57966-106">Das Cmdlet " **Get-AzureRemoteAppVNet** " Ruft Informationen zu virtuellen Azure RemoteApp-Netzwerken in Microsoft Azure ab.</span><span class="sxs-lookup"><span data-stu-id="57966-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="57966-107">Dieses Cmdlet gibt ein Objekt zurück, das Informationen zu einem angegebenen virtuellen Netzwerk enthält.</span><span class="sxs-lookup"><span data-stu-id="57966-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="57966-108">Wenn kein virtuelles Netzwerk angegeben ist, gibt dieses Cmdlet Informationen zu allen virtuellen Netzwerken im aktuellen Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="57966-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="57966-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57966-109">EXAMPLES</span></span>

### <span data-ttu-id="57966-110">Beispiel 1: Abrufen von Informationen zu einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="57966-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="57966-111">Dieser Befehl ruft Informationen über das virtuelle Netzwerk mit dem Namen ContosoVNet ab.</span><span class="sxs-lookup"><span data-stu-id="57966-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="57966-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="57966-112">PARAMETERS</span></span>

### <span data-ttu-id="57966-113">-IncludeSharedKey</span><span class="sxs-lookup"><span data-stu-id="57966-113">-IncludeSharedKey</span></span>
<span data-ttu-id="57966-114">Gibt an, dass dieses Cmdlet den Wert des freigegebenen Schlüssels in den Informationen enthält, die er über das virtuelle Netzwerk abruft.</span><span class="sxs-lookup"><span data-stu-id="57966-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57966-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="57966-115">-Profile</span></span>
<span data-ttu-id="57966-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="57966-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="57966-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="57966-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="57966-118">-VNetName</span><span class="sxs-lookup"><span data-stu-id="57966-118">-VNetName</span></span>
<span data-ttu-id="57966-119">Gibt den Namen des virtuellen Azure RemoteApp-Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="57966-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="57966-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57966-120">CommonParameters</span></span>
<span data-ttu-id="57966-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57966-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57966-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57966-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57966-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57966-123">INPUTS</span></span>

## <span data-ttu-id="57966-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57966-124">OUTPUTS</span></span>

## <span data-ttu-id="57966-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="57966-125">NOTES</span></span>

## <span data-ttu-id="57966-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57966-126">RELATED LINKS</span></span>

[<span data-ttu-id="57966-127">Satz-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="57966-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


