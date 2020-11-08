---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178383"
---
# <span data-ttu-id="c3a7e-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="c3a7e-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="c3a7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a7e-103">Viel aggregierte Benachrichtigung entlassen</span><span class="sxs-lookup"><span data-stu-id="c3a7e-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="c3a7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3a7e-104">SYNTAX</span></span>

### <span data-ttu-id="c3a7e-105">SolutionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3a7e-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3a7e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c3a7e-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3a7e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3a7e-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3a7e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3a7e-108">DESCRIPTION</span></span>
<span data-ttu-id="c3a7e-109">Mit dem Disable-AzIotSecurityAnalyticsAggregatedAlert-Cmdlet wird eine bestimmte aggragated-Warnung auf Geräten von viel Hub geschlossen.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="c3a7e-110">Der Name der aggregierten Alerts ist eine Kombination aus dem Warnungstyp und dem Warnungs aggragted Datum, getrennt durch "/".</span><span class="sxs-lookup"><span data-stu-id="c3a7e-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="c3a7e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3a7e-111">EXAMPLES</span></span>

### <span data-ttu-id="c3a7e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3a7e-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="c3a7e-113">Zusammengefasste Warnung "IoT_SucessfulLocalLogin/2020-03-15" (Name kombiniert mit dem Warnungstyp und dem aggregierten Datum) aus der Sicherheitslösung "MySolutionName" in der Ressourcengruppe "myresourcegroup" entlassen</span><span class="sxs-lookup"><span data-stu-id="c3a7e-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="c3a7e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c3a7e-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="c3a7e-115">Zusammengefasste Benachrichtigung mit Ressourcen-ID "/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/ResourceGroups/myresourcegroup/Providers/Microsoft.Security/iotsecuritysolutions/MySolutionName/analyticsmodels/default/aggregatedalerts/IoT_SucessfulLocalLogin/2020-03-15" schließen</span><span class="sxs-lookup"><span data-stu-id="c3a7e-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="c3a7e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3a7e-116">PARAMETERS</span></span>

### <span data-ttu-id="c3a7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a7e-117">-DefaultProfile</span></span>
<span data-ttu-id="c3a7e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3a7e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3a7e-119">-InputObject</span></span>
<span data-ttu-id="c3a7e-120">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a7e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c3a7e-121">-Name</span></span>
<span data-ttu-id="c3a7e-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="c3a7e-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3a7e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3a7e-123">-PassThru</span></span>
<span data-ttu-id="c3a7e-124">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="c3a7e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3a7e-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3a7e-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3a7e-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c3a7e-127">-ResourceId</span></span>
<span data-ttu-id="c3a7e-128">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a7e-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="c3a7e-129">-SolutionName</span></span>
<span data-ttu-id="c3a7e-130">Projektmappenname</span><span class="sxs-lookup"><span data-stu-id="c3a7e-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3a7e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3a7e-131">-Confirm</span></span>
<span data-ttu-id="c3a7e-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3a7e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3a7e-133">-WhatIf</span></span>
<span data-ttu-id="c3a7e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3a7e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3a7e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a7e-136">CommonParameters</span></span>
<span data-ttu-id="c3a7e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3a7e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a7e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3a7e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a7e-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3a7e-139">INPUTS</span></span>

### <span data-ttu-id="c3a7e-140">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="c3a7e-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="c3a7e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c3a7e-141">System.String</span></span>

## <span data-ttu-id="c3a7e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3a7e-142">OUTPUTS</span></span>

### <span data-ttu-id="c3a7e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3a7e-143">System.Boolean</span></span>

## <span data-ttu-id="c3a7e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3a7e-144">NOTES</span></span>

## <span data-ttu-id="c3a7e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3a7e-145">RELATED LINKS</span></span>
