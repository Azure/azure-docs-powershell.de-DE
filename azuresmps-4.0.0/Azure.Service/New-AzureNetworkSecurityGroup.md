---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006116"
---
# <span data-ttu-id="ca04d-101">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca04d-101">New-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="ca04d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca04d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca04d-103">Erstellt eine Azure Network Security-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ca04d-103">Creates an Azure network security group.</span></span>

## <span data-ttu-id="ca04d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca04d-104">SYNTAX</span></span>

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca04d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca04d-105">DESCRIPTION</span></span>
<span data-ttu-id="ca04d-106">Das Cmdlet **New-AzureNetworkSecurityGroup** erstellt eine Azure Network Security-Gruppe an einem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="ca04d-106">The **New-AzureNetworkSecurityGroup** cmdlet creates an Azure network security group in a location.</span></span>

## <span data-ttu-id="ca04d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca04d-107">EXAMPLES</span></span>

## <span data-ttu-id="ca04d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca04d-108">PARAMETERS</span></span>

### <span data-ttu-id="ca04d-109">-Label</span><span class="sxs-lookup"><span data-stu-id="ca04d-109">-Label</span></span>
<span data-ttu-id="ca04d-110">Gibt eine Beschreibung für die neue Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="ca04d-110">Specifies a description for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca04d-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="ca04d-111">-Location</span></span>
<span data-ttu-id="ca04d-112">Gibt den Azure-Speicherort an, an dem dieses Cmdlet eine Netzwerksicherheitsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="ca04d-112">Specifies the Azure location in which this cmdlet creates a network security group.</span></span>
<span data-ttu-id="ca04d-113">Verwenden Sie das Get-AzureLocation-Cmdlet, um gültige Speicherorte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ca04d-113">To obtain valid locations, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca04d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ca04d-114">-Name</span></span>
<span data-ttu-id="ca04d-115">Gibt einen Namen für die neue Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="ca04d-115">Specifies a name for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca04d-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="ca04d-116">-Profile</span></span>
<span data-ttu-id="ca04d-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ca04d-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ca04d-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ca04d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ca04d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca04d-119">CommonParameters</span></span>
<span data-ttu-id="ca04d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca04d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca04d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca04d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca04d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca04d-122">INPUTS</span></span>

## <span data-ttu-id="ca04d-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca04d-123">OUTPUTS</span></span>

## <span data-ttu-id="ca04d-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca04d-124">NOTES</span></span>

## <span data-ttu-id="ca04d-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca04d-125">RELATED LINKS</span></span>

[<span data-ttu-id="ca04d-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca04d-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)


