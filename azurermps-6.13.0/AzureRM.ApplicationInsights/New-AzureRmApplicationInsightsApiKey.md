---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: c60caa54f11fb2466631cf956cdc374b72265443
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480637"
---
# <span data-ttu-id="c9f28-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c9f28-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c9f28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9f28-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f28-103">Erstellen eines API-Schlüssels für Application Insights für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="c9f28-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9f28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9f28-104">SYNTAX</span></span>

### <span data-ttu-id="c9f28-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9f28-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f28-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9f28-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f28-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9f28-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9f28-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9f28-108">DESCRIPTION</span></span>
<span data-ttu-id="c9f28-109">Erstellen einer API-Schlüssel für Application Insights für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="c9f28-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="c9f28-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9f28-110">EXAMPLES</span></span>

### <span data-ttu-id="c9f28-111">Beispiel 1 Erstellen eines neuen API-Schlüssels für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="c9f28-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="c9f28-112">Erstellen Sie eine API-Schlüssel Beschreibung für Application Insights als "testapiKey" mit den Berechtigungen "ReadTelemetry", "WriteAnnotations" für die Ressource "Test" in der Ressourcengruppe "Testgruppe".</span><span class="sxs-lookup"><span data-stu-id="c9f28-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c9f28-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9f28-113">PARAMETERS</span></span>

### <span data-ttu-id="c9f28-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c9f28-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c9f28-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="c9f28-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c9f28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f28-116">-DefaultProfile</span></span>
<span data-ttu-id="c9f28-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9f28-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f28-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9f28-118">-Description</span></span>
<span data-ttu-id="c9f28-119">Beschreibung, um diesen API-Schlüssel zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c9f28-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="c9f28-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c9f28-120">-Name</span></span>
<span data-ttu-id="c9f28-121">Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="c9f28-121">Component Name.</span></span>

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

### <span data-ttu-id="c9f28-122">-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="c9f28-122">-Permissions</span></span>
<span data-ttu-id="c9f28-123">Berechtigungen, die von der API-Taste für apps zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="c9f28-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="c9f28-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f28-124">-ResourceGroupName</span></span>
<span data-ttu-id="c9f28-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c9f28-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c9f28-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c9f28-126">-ResourceId</span></span>
<span data-ttu-id="c9f28-127">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c9f28-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c9f28-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9f28-128">-Confirm</span></span>
<span data-ttu-id="c9f28-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9f28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f28-130">-WhatIf</span></span>
<span data-ttu-id="c9f28-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9f28-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9f28-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9f28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f28-133">CommonParameters</span></span>
<span data-ttu-id="c9f28-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f28-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9f28-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f28-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9f28-136">INPUTS</span></span>

### <span data-ttu-id="c9f28-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c9f28-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="c9f28-138">Parameter: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9f28-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="c9f28-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c9f28-139">System.String</span></span>

## <span data-ttu-id="c9f28-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9f28-140">OUTPUTS</span></span>

### <span data-ttu-id="c9f28-141">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="c9f28-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="c9f28-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9f28-142">NOTES</span></span>

## <span data-ttu-id="c9f28-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9f28-143">RELATED LINKS</span></span>
