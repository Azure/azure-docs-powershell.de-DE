---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 32e40bf33ac5f79529f7924b604998c97d004bef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936776"
---
# <span data-ttu-id="bd70b-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="bd70b-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="bd70b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd70b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd70b-103">ListenkonfigurationAssignments für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="bd70b-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="bd70b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd70b-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd70b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd70b-105">DESCRIPTION</span></span>
<span data-ttu-id="bd70b-106">ListenkonfigurationAssignments für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="bd70b-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="bd70b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd70b-107">EXAMPLES</span></span>

### <span data-ttu-id="bd70b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd70b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="bd70b-109">ListenkonfigurationAssignments für dedizierten Host.</span><span class="sxs-lookup"><span data-stu-id="bd70b-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="bd70b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bd70b-110">PARAMETERS</span></span>

### <span data-ttu-id="bd70b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd70b-111">-DefaultProfile</span></span>
<span data-ttu-id="bd70b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd70b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd70b-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="bd70b-113">-ProviderName</span></span>
<span data-ttu-id="bd70b-114">Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="bd70b-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd70b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd70b-115">-ResourceGroupName</span></span>
<span data-ttu-id="bd70b-116">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="bd70b-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd70b-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bd70b-117">-ResourceName</span></span>
<span data-ttu-id="bd70b-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="bd70b-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd70b-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="bd70b-119">-ResourceParentName</span></span>
<span data-ttu-id="bd70b-120">Der übergeordnete Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="bd70b-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd70b-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="bd70b-121">-ResourceParentType</span></span>
<span data-ttu-id="bd70b-122">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="bd70b-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd70b-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bd70b-123">-ResourceType</span></span>
<span data-ttu-id="bd70b-124">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="bd70b-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd70b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd70b-125">CommonParameters</span></span>
<span data-ttu-id="bd70b-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd70b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd70b-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd70b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd70b-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd70b-128">INPUTS</span></span>

### <span data-ttu-id="bd70b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bd70b-129">System.String</span></span>

## <span data-ttu-id="bd70b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd70b-130">OUTPUTS</span></span>

### <span data-ttu-id="bd70b-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="bd70b-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="bd70b-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bd70b-132">NOTES</span></span>

## <span data-ttu-id="bd70b-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bd70b-133">RELATED LINKS</span></span>
