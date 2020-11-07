---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: d04b2e54e10a88edd3273ecd96697ab993e97c98
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658110"
---
# <span data-ttu-id="5e104-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5e104-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="5e104-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e104-102">SYNOPSIS</span></span>
<span data-ttu-id="5e104-103">Erstellen einer neuen Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="5e104-103">Create a new application insights resource</span></span>

## <span data-ttu-id="5e104-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e104-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e104-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e104-105">DESCRIPTION</span></span>
<span data-ttu-id="5e104-106">Erstellen einer neuen Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="5e104-106">Create a new application insights resource</span></span>

## <span data-ttu-id="5e104-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e104-107">EXAMPLES</span></span>

### <span data-ttu-id="5e104-108">Beispiel 1 Erstellen einer neuen Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="5e104-108">Example 1 Create a new application insights resource</span></span>
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
```

<span data-ttu-id="5e104-109">Fügen Sie eine neue Application Insights-Ressource mit dem Namen "Test" in der Ressourcengruppe "testgroup" mit der Art "Java" hinzu.</span><span class="sxs-lookup"><span data-stu-id="5e104-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="5e104-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e104-110">PARAMETERS</span></span>

### <span data-ttu-id="5e104-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e104-111">-DefaultProfile</span></span>
<span data-ttu-id="5e104-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e104-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e104-113">-Art</span><span class="sxs-lookup"><span data-stu-id="5e104-113">-Kind</span></span>
<span data-ttu-id="5e104-114">Anwendung Art.</span><span class="sxs-lookup"><span data-stu-id="5e104-114">Application kind.</span></span>

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

### <span data-ttu-id="5e104-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="5e104-115">-Location</span></span>
<span data-ttu-id="5e104-116">Application Insights-Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="5e104-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="5e104-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5e104-117">-Name</span></span>
<span data-ttu-id="5e104-118">Ressourcen Name für Application Insights</span><span class="sxs-lookup"><span data-stu-id="5e104-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="5e104-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e104-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e104-120">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e104-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="5e104-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="5e104-121">-Tag</span></span>
<span data-ttu-id="5e104-122">Komponentenkategorien.</span><span class="sxs-lookup"><span data-stu-id="5e104-122">Component Tags.</span></span>

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

### <span data-ttu-id="5e104-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e104-123">-Confirm</span></span>
<span data-ttu-id="5e104-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e104-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e104-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e104-125">-WhatIf</span></span>
<span data-ttu-id="5e104-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e104-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e104-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e104-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e104-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e104-128">CommonParameters</span></span>
<span data-ttu-id="5e104-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e104-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e104-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e104-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e104-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e104-131">INPUTS</span></span>

### <span data-ttu-id="5e104-132">Keine</span><span class="sxs-lookup"><span data-stu-id="5e104-132">None</span></span>

## <span data-ttu-id="5e104-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e104-133">OUTPUTS</span></span>

### <span data-ttu-id="5e104-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5e104-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="5e104-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e104-135">NOTES</span></span>

## <span data-ttu-id="5e104-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e104-136">RELATED LINKS</span></span>
