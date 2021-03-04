---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: a4625d48086064fb59b5f2faee78357380f6a323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944051"
---
# <span data-ttu-id="e68ca-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="e68ca-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="e68ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e68ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e68ca-103">Konfigurationsdatensatz für öffentliche Wartung</span><span class="sxs-lookup"><span data-stu-id="e68ca-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="e68ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e68ca-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e68ca-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e68ca-105">DESCRIPTION</span></span>
<span data-ttu-id="e68ca-106">Konfigurationsdatensatz für öffentliche Wartung</span><span class="sxs-lookup"><span data-stu-id="e68ca-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="e68ca-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e68ca-107">EXAMPLES</span></span>

### <span data-ttu-id="e68ca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e68ca-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="e68ca-109">Konfigurationsdatensatz für öffentliche Wartung</span><span class="sxs-lookup"><span data-stu-id="e68ca-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="e68ca-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e68ca-110">PARAMETERS</span></span>

### <span data-ttu-id="e68ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68ca-111">-DefaultProfile</span></span>
<span data-ttu-id="e68ca-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e68ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e68ca-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e68ca-113">-Name</span></span>
<span data-ttu-id="e68ca-114">Name der Konfiguration der öffentlichen Wartung.</span><span class="sxs-lookup"><span data-stu-id="e68ca-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e68ca-115">-ResourceGroupName</span></span>
<span data-ttu-id="e68ca-116">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e68ca-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68ca-117">CommonParameters</span></span>
<span data-ttu-id="e68ca-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e68ca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68ca-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e68ca-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68ca-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e68ca-120">INPUTS</span></span>

### <span data-ttu-id="e68ca-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e68ca-121">System.String</span></span>

## <span data-ttu-id="e68ca-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e68ca-122">OUTPUTS</span></span>

### <span data-ttu-id="e68ca-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e68ca-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="e68ca-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e68ca-124">NOTES</span></span>

## <span data-ttu-id="e68ca-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e68ca-125">RELATED LINKS</span></span>
