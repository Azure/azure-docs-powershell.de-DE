---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
ms.openlocfilehash: 545047eea1451d5c03bba9db805c1d5a1a928e08
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849491"
---
# <span data-ttu-id="2df19-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="2df19-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="2df19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2df19-102">SYNOPSIS</span></span>
<span data-ttu-id="2df19-103">Ruft den Bereitstellungsvorgang der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2df19-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2df19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2df19-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2df19-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2df19-105">DESCRIPTION</span></span>
<span data-ttu-id="2df19-106">Das Cmdlet " **Get-AzureRmResourceGroupDeploymentOperation** " listet alle Vorgänge auf, die Teil einer Bereitstellung waren, damit Sie weitere Informationen zu den exakten Vorgängen finden können, die für eine bestimmte Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="2df19-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="2df19-107">Außerdem kann die Antwort und der Anforderungs Inhalt für jeden Bereitstellungsvorgang angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2df19-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="2df19-108">Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2df19-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="2df19-109">Um die Anforderung und den Antwortinhalt abzurufen, aktivieren Sie diese Einstellung, wenn Sie eine Bereitstellung über **New-AzureRmResourceGroupDeployment** übermitteln.</span><span class="sxs-lookup"><span data-stu-id="2df19-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="2df19-110">Sie kann potenziell Geheimnisse wie Kennwörter protokollieren und verfügbar machen, die in den Ressourceneigenschaften-oder **listKeys** -Vorgängen verwendet werden, die beim Abrufen der Bereitstellungsvorgänge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2df19-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="2df19-111">Weitere Informationen zu dieser Einstellung und dazu, wie Sie Sie aktivieren, finden Sie unter New-AzureRmResourceGroupDeployment und Debuggen von Arm-Vorlagen Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="2df19-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="2df19-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2df19-112">EXAMPLES</span></span>

### <span data-ttu-id="2df19-113">Get1</span><span class="sxs-lookup"><span data-stu-id="2df19-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="2df19-114">Ruft den Bereitstellungsvorgang mit dem Namen "Test" unter Ressourcengruppe "Test" ab</span><span class="sxs-lookup"><span data-stu-id="2df19-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="2df19-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2df19-115">PARAMETERS</span></span>

### <span data-ttu-id="2df19-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2df19-116">-ApiVersion</span></span>
<span data-ttu-id="2df19-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2df19-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2df19-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2df19-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2df19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df19-119">-DefaultProfile</span></span>
<span data-ttu-id="2df19-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2df19-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2df19-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="2df19-121">-DeploymentName</span></span>
<span data-ttu-id="2df19-122">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="2df19-122">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df19-123">-Information</span><span class="sxs-lookup"><span data-stu-id="2df19-123">-InformationAction</span></span>
<span data-ttu-id="2df19-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="2df19-124">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="2df19-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2df19-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2df19-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="2df19-126">Continue</span></span>
- <span data-ttu-id="2df19-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="2df19-127">Ignore</span></span>
- <span data-ttu-id="2df19-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="2df19-128">Inquire</span></span>
- <span data-ttu-id="2df19-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2df19-129">SilentlyContinue</span></span>
- <span data-ttu-id="2df19-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="2df19-130">Stop</span></span>
- <span data-ttu-id="2df19-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="2df19-131">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df19-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2df19-132">-InformationVariable</span></span>
<span data-ttu-id="2df19-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="2df19-133">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df19-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="2df19-134">-Pre</span></span>
<span data-ttu-id="2df19-135">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="2df19-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2df19-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df19-136">-ResourceGroupName</span></span>
<span data-ttu-id="2df19-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2df19-137">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df19-138">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2df19-138">-SubscriptionId</span></span>
<span data-ttu-id="2df19-139">Das zu verwendende Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2df19-139">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2df19-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df19-140">CommonParameters</span></span>
<span data-ttu-id="2df19-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df19-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df19-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df19-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df19-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2df19-143">INPUTS</span></span>

## <span data-ttu-id="2df19-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2df19-144">OUTPUTS</span></span>

## <span data-ttu-id="2df19-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2df19-145">NOTES</span></span>

## <span data-ttu-id="2df19-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2df19-146">RELATED LINKS</span></span>
