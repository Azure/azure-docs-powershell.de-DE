---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174344"
---
# <span data-ttu-id="731a1-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="731a1-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="731a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="731a1-102">SYNOPSIS</span></span>
<span data-ttu-id="731a1-103">Abrufen eines Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="731a1-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="731a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="731a1-104">SYNTAX</span></span>

### <span data-ttu-id="731a1-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="731a1-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="731a1-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="731a1-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="731a1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="731a1-107">DESCRIPTION</span></span>
<span data-ttu-id="731a1-108">Das Cmdlet " **Get-AzIpGroup** " Ruft ein Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="731a1-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="731a1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="731a1-109">EXAMPLES</span></span>

### <span data-ttu-id="731a1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="731a1-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="731a1-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="731a1-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="731a1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="731a1-112">PARAMETERS</span></span>

### <span data-ttu-id="731a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731a1-113">-DefaultProfile</span></span>
<span data-ttu-id="731a1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="731a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731a1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="731a1-115">-Name</span></span>
<span data-ttu-id="731a1-116">Der Name des ipgroup.</span><span class="sxs-lookup"><span data-stu-id="731a1-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="731a1-118">Der Ressourcengruppenname des ipgroup.</span><span class="sxs-lookup"><span data-stu-id="731a1-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731a1-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="731a1-119">-ResourceId</span></span>
<span data-ttu-id="731a1-120">Ipgroup.</span><span class="sxs-lookup"><span data-stu-id="731a1-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731a1-121">CommonParameters</span></span>
<span data-ttu-id="731a1-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="731a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731a1-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="731a1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731a1-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="731a1-124">INPUTS</span></span>

### <span data-ttu-id="731a1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="731a1-125">System.String</span></span>

## <span data-ttu-id="731a1-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="731a1-126">OUTPUTS</span></span>

### <span data-ttu-id="731a1-127">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="731a1-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="731a1-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="731a1-128">NOTES</span></span>

## <span data-ttu-id="731a1-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="731a1-129">RELATED LINKS</span></span>
