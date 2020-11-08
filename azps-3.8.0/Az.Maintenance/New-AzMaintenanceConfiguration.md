---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004426"
---
# <span data-ttu-id="2466e-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2466e-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="2466e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2466e-102">SYNOPSIS</span></span>
<span data-ttu-id="2466e-103">Erstellen oder Aktualisieren eines Konfigurationseintrags</span><span class="sxs-lookup"><span data-stu-id="2466e-103">Create or Update configuration record</span></span>

## <span data-ttu-id="2466e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2466e-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2466e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2466e-105">DESCRIPTION</span></span>
<span data-ttu-id="2466e-106">Erstellen oder Aktualisieren eines Konfigurationseintrags</span><span class="sxs-lookup"><span data-stu-id="2466e-106">Create or Update configuration record</span></span>

## <span data-ttu-id="2466e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2466e-107">EXAMPLES</span></span>

### <span data-ttu-id="2466e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2466e-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="2466e-109">Erstellen einer Wartungs Konfiguration mit Scope-Host</span><span class="sxs-lookup"><span data-stu-id="2466e-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="2466e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2466e-110">PARAMETERS</span></span>

### <span data-ttu-id="2466e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2466e-111">-AsJob</span></span>
<span data-ttu-id="2466e-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2466e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2466e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2466e-113">-DefaultProfile</span></span>
<span data-ttu-id="2466e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2466e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2466e-115">-Extensionproperty</span><span class="sxs-lookup"><span data-stu-id="2466e-115">-ExtensionProperty</span></span>
<span data-ttu-id="2466e-116">Die Erweiterungseigenschaften pro Ressource.</span><span class="sxs-lookup"><span data-stu-id="2466e-116">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2466e-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="2466e-117">-Location</span></span>
<span data-ttu-id="2466e-118">Der Speicherort der Wartungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2466e-118">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="2466e-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="2466e-119">-MaintenanceScope</span></span>
<span data-ttu-id="2466e-120">Der Wartungsbereich.</span><span class="sxs-lookup"><span data-stu-id="2466e-120">The Maintenance Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2466e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2466e-121">-Name</span></span>
<span data-ttu-id="2466e-122">Der Name der Wartungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2466e-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="2466e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2466e-123">-ResourceGroupName</span></span>
<span data-ttu-id="2466e-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2466e-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="2466e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2466e-125">-Tag</span></span>
<span data-ttu-id="2466e-126">Die Arm-Tags.</span><span class="sxs-lookup"><span data-stu-id="2466e-126">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2466e-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2466e-127">-Confirm</span></span>
<span data-ttu-id="2466e-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2466e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2466e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2466e-129">-WhatIf</span></span>
<span data-ttu-id="2466e-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2466e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2466e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2466e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2466e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2466e-132">CommonParameters</span></span>
<span data-ttu-id="2466e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2466e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2466e-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2466e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2466e-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2466e-135">INPUTS</span></span>

### <span data-ttu-id="2466e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2466e-136">System.String</span></span>

## <span data-ttu-id="2466e-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2466e-137">OUTPUTS</span></span>

### <span data-ttu-id="2466e-138">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2466e-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="2466e-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="2466e-139">NOTES</span></span>

## <span data-ttu-id="2466e-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2466e-140">RELATED LINKS</span></span>
