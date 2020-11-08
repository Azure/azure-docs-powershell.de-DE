---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004421"
---
# <span data-ttu-id="e7c83-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7c83-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="e7c83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7c83-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c83-103">Patch-Konfigurationseintrag</span><span class="sxs-lookup"><span data-stu-id="e7c83-103">Patch configuration record</span></span>

## <span data-ttu-id="e7c83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7c83-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7c83-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7c83-105">DESCRIPTION</span></span>
<span data-ttu-id="e7c83-106">Patch Maintenance-Konfigurationseintrag</span><span class="sxs-lookup"><span data-stu-id="e7c83-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="e7c83-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7c83-107">EXAMPLES</span></span>

### <span data-ttu-id="e7c83-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7c83-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="e7c83-109">Patch Maintenance-Konfigurationseintrag</span><span class="sxs-lookup"><span data-stu-id="e7c83-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="e7c83-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7c83-110">PARAMETERS</span></span>

### <span data-ttu-id="e7c83-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7c83-111">-AsJob</span></span>
<span data-ttu-id="e7c83-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e7c83-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c83-113">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e7c83-113">-Configuration</span></span>
<span data-ttu-id="e7c83-114">Die Wartungs Konfiguration, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7c83-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c83-115">-DefaultProfile</span></span>
<span data-ttu-id="e7c83-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7c83-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7c83-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e7c83-117">-Name</span></span>
<span data-ttu-id="e7c83-118">Der Name der Wartungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e7c83-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="e7c83-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7c83-119">-ResourceGroupName</span></span>
<span data-ttu-id="e7c83-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e7c83-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="e7c83-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7c83-121">-Confirm</span></span>
<span data-ttu-id="e7c83-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7c83-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c83-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7c83-123">-WhatIf</span></span>
<span data-ttu-id="e7c83-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7c83-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7c83-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7c83-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c83-126">CommonParameters</span></span>
<span data-ttu-id="e7c83-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c83-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7c83-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c83-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7c83-129">INPUTS</span></span>

### <span data-ttu-id="e7c83-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e7c83-130">System.String</span></span>

### <span data-ttu-id="e7c83-131">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7c83-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="e7c83-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7c83-132">OUTPUTS</span></span>

### <span data-ttu-id="e7c83-133">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7c83-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="e7c83-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7c83-134">NOTES</span></span>

## <span data-ttu-id="e7c83-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7c83-135">RELATED LINKS</span></span>
