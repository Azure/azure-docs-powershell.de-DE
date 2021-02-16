---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149508"
---
# <span data-ttu-id="4bac4-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="4bac4-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="4bac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bac4-102">SYNOPSIS</span></span>
<span data-ttu-id="4bac4-103">Erstellen eines API-Schlüssels für Anwendungserkenntnisse für eine Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="4bac4-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="4bac4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bac4-104">SYNTAX</span></span>

### <span data-ttu-id="4bac4-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4bac4-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bac4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bac4-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bac4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bac4-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bac4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bac4-108">DESCRIPTION</span></span>
<span data-ttu-id="4bac4-109">Erstellen von API-Schlüsseln für Anwendungserkenntnisse für eine Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="4bac4-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="4bac4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4bac4-110">EXAMPLES</span></span>

### <span data-ttu-id="4bac4-111">Beispiel 1: Erstellen eines neuen API-Schlüssels für eine Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="4bac4-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="4bac4-112">Erstellen Sie eine Api-Schlüsselbeschreibung für Anwendungserkenntnisse als "testapiKey" mit den Berechtigungen "ReadTelemetry", "WriteAnnotations" für den Ressourcentest in der Ressourcengruppe "testGroup".</span><span class="sxs-lookup"><span data-stu-id="4bac4-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="4bac4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bac4-113">PARAMETERS</span></span>

### <span data-ttu-id="4bac4-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4bac4-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="4bac4-115">Anwendungserkenntnisse-Komponentenobjekt.</span><span class="sxs-lookup"><span data-stu-id="4bac4-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="4bac4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bac4-116">-DefaultProfile</span></span>
<span data-ttu-id="4bac4-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bac4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bac4-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bac4-118">-Description</span></span>
<span data-ttu-id="4bac4-119">Beschreibung zur Identifizierung dieses API-Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="4bac4-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="4bac4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4bac4-120">-Name</span></span>
<span data-ttu-id="4bac4-121">Komponentenname.</span><span class="sxs-lookup"><span data-stu-id="4bac4-121">Component Name.</span></span>

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

### <span data-ttu-id="4bac4-122">-Permissions</span><span class="sxs-lookup"><span data-stu-id="4bac4-122">-Permissions</span></span>
<span data-ttu-id="4bac4-123">Berechtigungen, die mit dem API-Schlüssel apps ermöglicht werden können.</span><span class="sxs-lookup"><span data-stu-id="4bac4-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="4bac4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bac4-124">-ResourceGroupName</span></span>
<span data-ttu-id="4bac4-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="4bac4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4bac4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bac4-126">-ResourceId</span></span>
<span data-ttu-id="4bac4-127">Ressourcen-ID der Komponente für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="4bac4-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="4bac4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bac4-128">-Confirm</span></span>
<span data-ttu-id="4bac4-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bac4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bac4-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4bac4-130">-WhatIf</span></span>
<span data-ttu-id="4bac4-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bac4-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bac4-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bac4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bac4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bac4-133">CommonParameters</span></span>
<span data-ttu-id="4bac4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bac4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bac4-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bac4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bac4-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4bac4-136">INPUTS</span></span>

### <span data-ttu-id="4bac4-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4bac4-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="4bac4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4bac4-138">System.String</span></span>

## <span data-ttu-id="4bac4-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4bac4-139">OUTPUTS</span></span>

### <span data-ttu-id="4bac4-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="4bac4-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="4bac4-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4bac4-141">NOTES</span></span>

## <span data-ttu-id="4bac4-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4bac4-142">RELATED LINKS</span></span>
