---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177128"
---
# <span data-ttu-id="4dea6-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4dea6-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="4dea6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4dea6-102">SYNOPSIS</span></span>
<span data-ttu-id="4dea6-103">Erstellen einer neuen Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="4dea6-103">Create a new application insights resource</span></span>

## <span data-ttu-id="4dea6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dea6-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4dea6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dea6-105">DESCRIPTION</span></span>
<span data-ttu-id="4dea6-106">Erstellen einer neuen Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="4dea6-106">Create a new application insights resource</span></span>

## <span data-ttu-id="4dea6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4dea6-107">EXAMPLES</span></span>

### <span data-ttu-id="4dea6-108">Beispiel 1 Erstellen einer neuen Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="4dea6-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="4dea6-109">Hinzufügen einer neuen Application Insights-Ressource mit dem Namen "Test" in der Ressourcengruppe "Testgruppe" mit der Art "Java"</span><span class="sxs-lookup"><span data-stu-id="4dea6-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="4dea6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dea6-110">PARAMETERS</span></span>

### <span data-ttu-id="4dea6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dea6-111">-DefaultProfile</span></span>
<span data-ttu-id="4dea6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4dea6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dea6-113">-Art</span><span class="sxs-lookup"><span data-stu-id="4dea6-113">-Kind</span></span>
<span data-ttu-id="4dea6-114">Anwendung Art.</span><span class="sxs-lookup"><span data-stu-id="4dea6-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dea6-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="4dea6-115">-Location</span></span>
<span data-ttu-id="4dea6-116">Application Insights-Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="4dea6-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dea6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4dea6-117">-Name</span></span>
<span data-ttu-id="4dea6-118">Ressourcen Name für Application Insights</span><span class="sxs-lookup"><span data-stu-id="4dea6-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dea6-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="4dea6-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="4dea6-120">Der Netzwerkzugriffstyp für den Zugriff auf die Einnahme von Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4dea6-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="4dea6-121">Der Wert sollte "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="4dea6-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dea6-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="4dea6-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="4dea6-123">Der Netzwerkzugriffstyp für den Zugriff auf die Abfrage von Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4dea6-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="4dea6-124">Der Wert sollte "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="4dea6-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dea6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dea6-125">-ResourceGroupName</span></span>
<span data-ttu-id="4dea6-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4dea6-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dea6-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4dea6-127">-RetentionInDays</span></span>
<span data-ttu-id="4dea6-128">Aufbewahrung in Tagen, 90 standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="4dea6-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dea6-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="4dea6-129">-Tag</span></span>
<span data-ttu-id="4dea6-130">Komponentenkategorien.</span><span class="sxs-lookup"><span data-stu-id="4dea6-130">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dea6-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4dea6-131">-Confirm</span></span>
<span data-ttu-id="4dea6-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4dea6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dea6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dea6-133">-WhatIf</span></span>
<span data-ttu-id="4dea6-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4dea6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dea6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4dea6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dea6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dea6-136">CommonParameters</span></span>
<span data-ttu-id="4dea6-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dea6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dea6-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dea6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dea6-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4dea6-139">INPUTS</span></span>

### <span data-ttu-id="4dea6-140">Keine</span><span class="sxs-lookup"><span data-stu-id="4dea6-140">None</span></span>

## <span data-ttu-id="4dea6-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4dea6-141">OUTPUTS</span></span>

### <span data-ttu-id="4dea6-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4dea6-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="4dea6-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="4dea6-143">NOTES</span></span>

## <span data-ttu-id="4dea6-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4dea6-144">RELATED LINKS</span></span>
