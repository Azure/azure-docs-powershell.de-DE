---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004430"
---
# <span data-ttu-id="96d1e-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="96d1e-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="96d1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="96d1e-103">Abrufen des Wartungs Konfigurationseintrags</span><span class="sxs-lookup"><span data-stu-id="96d1e-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="96d1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96d1e-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96d1e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="96d1e-106">Abrufen des Wartungs Konfigurationseintrags</span><span class="sxs-lookup"><span data-stu-id="96d1e-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="96d1e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96d1e-107">EXAMPLES</span></span>

### <span data-ttu-id="96d1e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="96d1e-108">Example 1</span></span>
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

<span data-ttu-id="96d1e-109">Abrufen des Wartungs Konfigurationseintrags</span><span class="sxs-lookup"><span data-stu-id="96d1e-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="96d1e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="96d1e-110">PARAMETERS</span></span>

### <span data-ttu-id="96d1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d1e-111">-DefaultProfile</span></span>
<span data-ttu-id="96d1e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96d1e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96d1e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="96d1e-113">-Name</span></span>
<span data-ttu-id="96d1e-114">Der Name der Wartungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="96d1e-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="96d1e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d1e-115">-ResourceGroupName</span></span>
<span data-ttu-id="96d1e-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="96d1e-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="96d1e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d1e-117">CommonParameters</span></span>
<span data-ttu-id="96d1e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d1e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d1e-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96d1e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d1e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96d1e-120">INPUTS</span></span>

### <span data-ttu-id="96d1e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="96d1e-121">System.String</span></span>

## <span data-ttu-id="96d1e-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96d1e-122">OUTPUTS</span></span>

### <span data-ttu-id="96d1e-123">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="96d1e-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="96d1e-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="96d1e-124">NOTES</span></span>

## <span data-ttu-id="96d1e-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96d1e-125">RELATED LINKS</span></span>
