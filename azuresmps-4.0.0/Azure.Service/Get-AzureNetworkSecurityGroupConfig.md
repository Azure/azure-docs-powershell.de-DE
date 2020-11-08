---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006539"
---
# <span data-ttu-id="1544b-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="1544b-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="1544b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1544b-102">SYNOPSIS</span></span>
<span data-ttu-id="1544b-103">Ruft Details für eine Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="1544b-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="1544b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1544b-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1544b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1544b-105">DESCRIPTION</span></span>
<span data-ttu-id="1544b-106">Das Cmdlet " **Get-AzureNetworkSecurityGroupConfig** " gibt Details für eine Netzwerksicherheitsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="1544b-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="1544b-107">Geben Sie den *detaillierten* Parameter an, um die Netzwerksicherheitsregeln anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1544b-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="1544b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1544b-108">EXAMPLES</span></span>

## <span data-ttu-id="1544b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1544b-109">PARAMETERS</span></span>

### <span data-ttu-id="1544b-110">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="1544b-110">-Detailed</span></span>
<span data-ttu-id="1544b-111">Gibt an, dass dieses Cmdlet die Netzwerksicherheitsregeln anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1544b-111">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="1544b-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="1544b-112">-Profile</span></span>
<span data-ttu-id="1544b-113">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1544b-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1544b-114">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1544b-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1544b-115">-VM</span><span class="sxs-lookup"><span data-stu-id="1544b-115">-VM</span></span>
<span data-ttu-id="1544b-116">Gibt den virtuellen Computer an, für den dieses Cmdlet die Details einer Netzwerksicherheitsgruppe abruft.</span><span class="sxs-lookup"><span data-stu-id="1544b-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1544b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1544b-117">CommonParameters</span></span>
<span data-ttu-id="1544b-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1544b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1544b-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1544b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1544b-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1544b-120">INPUTS</span></span>

## <span data-ttu-id="1544b-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1544b-121">OUTPUTS</span></span>

## <span data-ttu-id="1544b-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="1544b-122">NOTES</span></span>

## <span data-ttu-id="1544b-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1544b-123">RELATED LINKS</span></span>

[<span data-ttu-id="1544b-124">Neu – AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1544b-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="1544b-125">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1544b-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


