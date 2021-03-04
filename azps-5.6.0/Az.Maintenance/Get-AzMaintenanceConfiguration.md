---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: 6939cde26695cb4273d776437c3697c03d426db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934931"
---
# <span data-ttu-id="254d6-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="254d6-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="254d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="254d6-102">SYNOPSIS</span></span>
<span data-ttu-id="254d6-103">Wartungskonfigurationsdatensatz erhalten</span><span class="sxs-lookup"><span data-stu-id="254d6-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="254d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="254d6-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="254d6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="254d6-105">DESCRIPTION</span></span>
<span data-ttu-id="254d6-106">Wartungskonfigurationsdatensatz erhalten</span><span class="sxs-lookup"><span data-stu-id="254d6-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="254d6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="254d6-107">EXAMPLES</span></span>

### <span data-ttu-id="254d6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="254d6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="254d6-109">Wartungskonfigurationsdatensatz erhalten</span><span class="sxs-lookup"><span data-stu-id="254d6-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="254d6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="254d6-110">PARAMETERS</span></span>

### <span data-ttu-id="254d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254d6-111">-DefaultProfile</span></span>
<span data-ttu-id="254d6-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="254d6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="254d6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="254d6-113">-Name</span></span>
<span data-ttu-id="254d6-114">Name der Wartungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="254d6-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254d6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="254d6-115">-ResourceGroupName</span></span>
<span data-ttu-id="254d6-116">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="254d6-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254d6-117">CommonParameters</span></span>
<span data-ttu-id="254d6-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="254d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254d6-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="254d6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254d6-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="254d6-120">INPUTS</span></span>

### <span data-ttu-id="254d6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="254d6-121">System.String</span></span>

## <span data-ttu-id="254d6-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="254d6-122">OUTPUTS</span></span>

### <span data-ttu-id="254d6-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="254d6-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="254d6-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="254d6-124">NOTES</span></span>

## <span data-ttu-id="254d6-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="254d6-125">RELATED LINKS</span></span>
