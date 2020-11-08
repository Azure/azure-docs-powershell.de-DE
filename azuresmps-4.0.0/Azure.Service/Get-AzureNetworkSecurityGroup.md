---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006540"
---
# <span data-ttu-id="4198c-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4198c-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="4198c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4198c-102">SYNOPSIS</span></span>
<span data-ttu-id="4198c-103">Ruft Details für eine Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4198c-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="4198c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4198c-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4198c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4198c-105">DESCRIPTION</span></span>
<span data-ttu-id="4198c-106">Das Cmdlet " **Get-AzureNetworkSecurityGroup** " gibt Details für eine Azure Network Security-Gruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="4198c-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="4198c-107">Geben Sie den *detaillierten* Parameter an, um die Netzwerksicherheitsregeln anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4198c-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="4198c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4198c-108">EXAMPLES</span></span>

## <span data-ttu-id="4198c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4198c-109">PARAMETERS</span></span>

### <span data-ttu-id="4198c-110">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="4198c-110">-Detailed</span></span>
<span data-ttu-id="4198c-111">Gibt an, dass dieses Cmdlet die Netzwerksicherheitsregeln für die Netzwerksicherheitsgruppe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4198c-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

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

### <span data-ttu-id="4198c-112">-Name</span><span class="sxs-lookup"><span data-stu-id="4198c-112">-Name</span></span>
<span data-ttu-id="4198c-113">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4198c-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="4198c-114">Wenn eine klassische Netzwerksicherheitsgruppe in einer anderen Ressourcengruppe als ***Standard-Networking*** mithilfe des Azure-Portals erstellt wird, müssen Sie die folgende PowerShell-Syntax verwenden: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` .</span><span class="sxs-lookup"><span data-stu-id="4198c-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

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

### <span data-ttu-id="4198c-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="4198c-115">-Profile</span></span>
<span data-ttu-id="4198c-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4198c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4198c-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4198c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4198c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4198c-118">CommonParameters</span></span>
<span data-ttu-id="4198c-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4198c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4198c-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4198c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4198c-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4198c-121">INPUTS</span></span>

## <span data-ttu-id="4198c-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4198c-122">OUTPUTS</span></span>

## <span data-ttu-id="4198c-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="4198c-123">NOTES</span></span>

## <span data-ttu-id="4198c-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4198c-124">RELATED LINKS</span></span>

[<span data-ttu-id="4198c-125">Neu – AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4198c-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="4198c-126">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4198c-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

