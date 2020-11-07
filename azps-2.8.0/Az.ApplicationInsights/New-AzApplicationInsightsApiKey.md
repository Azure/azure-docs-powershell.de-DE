---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: c4f972971b52e6ff8e7bac4ebcb0850ef71846ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658108"
---
# <span data-ttu-id="ee325-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="ee325-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="ee325-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee325-102">SYNOPSIS</span></span>
<span data-ttu-id="ee325-103">Erstellen eines API-Schlüssels für Application Insights für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="ee325-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="ee325-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee325-104">SYNTAX</span></span>

### <span data-ttu-id="ee325-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee325-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee325-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee325-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee325-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee325-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee325-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee325-108">DESCRIPTION</span></span>
<span data-ttu-id="ee325-109">Erstellen einer API-Schlüssel für Application Insights für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="ee325-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="ee325-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee325-110">EXAMPLES</span></span>

### <span data-ttu-id="ee325-111">Beispiel 1 Erstellen eines neuen API-Schlüssels für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="ee325-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="ee325-112">Erstellen Sie eine API-Schlüssel Beschreibung für Application Insights als "testapiKey" mit den Berechtigungen "ReadTelemetry", "WriteAnnotations" für die Ressource "Test" in der Ressourcengruppe "Testgruppe".</span><span class="sxs-lookup"><span data-stu-id="ee325-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="ee325-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee325-113">PARAMETERS</span></span>

### <span data-ttu-id="ee325-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ee325-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ee325-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="ee325-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee325-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee325-116">-DefaultProfile</span></span>
<span data-ttu-id="ee325-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee325-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee325-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee325-118">-Description</span></span>
<span data-ttu-id="ee325-119">Beschreibung, um diesen API-Schlüssel zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ee325-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee325-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ee325-120">-Name</span></span>
<span data-ttu-id="ee325-121">Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="ee325-121">Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee325-122">-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="ee325-122">-Permissions</span></span>
<span data-ttu-id="ee325-123">Berechtigungen, die von der API-Taste für apps zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="ee325-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee325-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee325-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee325-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ee325-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee325-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ee325-126">-ResourceId</span></span>
<span data-ttu-id="ee325-127">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ee325-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee325-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ee325-128">-Confirm</span></span>
<span data-ttu-id="ee325-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee325-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee325-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee325-130">-WhatIf</span></span>
<span data-ttu-id="ee325-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee325-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee325-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee325-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee325-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee325-133">CommonParameters</span></span>
<span data-ttu-id="ee325-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee325-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee325-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee325-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee325-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee325-136">INPUTS</span></span>

### <span data-ttu-id="ee325-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ee325-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ee325-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ee325-138">System.String</span></span>

## <span data-ttu-id="ee325-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee325-139">OUTPUTS</span></span>

### <span data-ttu-id="ee325-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="ee325-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="ee325-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee325-141">NOTES</span></span>

## <span data-ttu-id="ee325-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee325-142">RELATED LINKS</span></span>
