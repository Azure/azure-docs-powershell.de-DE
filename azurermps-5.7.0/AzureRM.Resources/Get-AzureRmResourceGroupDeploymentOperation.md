---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: 557aa312200a2e5c49e33f8a176079ee4b27b629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480970"
---
# <span data-ttu-id="7db25-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7db25-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="7db25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7db25-102">SYNOPSIS</span></span>
<span data-ttu-id="7db25-103">Ruft den Bereitstellungsvorgang der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7db25-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7db25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7db25-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7db25-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7db25-105">DESCRIPTION</span></span>
<span data-ttu-id="7db25-106">Das Cmdlet " **Get-AzureRmResourceGroupDeploymentOperation** " listet alle Vorgänge auf, die Teil einer Bereitstellung waren, damit Sie weitere Informationen zu den exakten Vorgängen finden können, die für eine bestimmte Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="7db25-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="7db25-107">Außerdem kann die Antwort und der Anforderungs Inhalt für jeden Bereitstellungsvorgang angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7db25-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="7db25-108">Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7db25-108">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="7db25-109">Um die Anforderung und den Antwortinhalt abzurufen, aktivieren Sie diese Einstellung, wenn Sie eine Bereitstellung über **New-AzureRmResourceGroupDeployment** übermitteln.</span><span class="sxs-lookup"><span data-stu-id="7db25-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="7db25-110">Sie kann potenziell Geheimnisse wie Kennwörter protokollieren und verfügbar machen, die in den Ressourceneigenschaften-oder **listKeys** -Vorgängen verwendet werden, die beim Abrufen der Bereitstellungsvorgänge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7db25-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="7db25-111">Weitere Informationen zu dieser Einstellung und dazu, wie Sie Sie aktivieren, finden Sie unter New-AzureRmResourceGroupDeployment und Debuggen von Arm-Vorlagen Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="7db25-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="7db25-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7db25-112">EXAMPLES</span></span>

### <span data-ttu-id="7db25-113">Get1</span><span class="sxs-lookup"><span data-stu-id="7db25-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="7db25-114">Ruft den Bereitstellungsvorgang mit dem Namen "Test" unter Ressourcengruppe "Test" ab</span><span class="sxs-lookup"><span data-stu-id="7db25-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="7db25-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7db25-115">PARAMETERS</span></span>

### <span data-ttu-id="7db25-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7db25-116">-ApiVersion</span></span>
<span data-ttu-id="7db25-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7db25-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7db25-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7db25-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db25-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db25-119">-DefaultProfile</span></span>
<span data-ttu-id="7db25-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7db25-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db25-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="7db25-121">-DeploymentName</span></span>
<span data-ttu-id="7db25-122">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="7db25-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db25-123">-Information</span><span class="sxs-lookup"><span data-stu-id="7db25-123">-InformationAction</span></span>
<span data-ttu-id="7db25-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="7db25-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7db25-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7db25-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7db25-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="7db25-126">Continue</span></span>
- <span data-ttu-id="7db25-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="7db25-127">Ignore</span></span>
- <span data-ttu-id="7db25-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="7db25-128">Inquire</span></span>
- <span data-ttu-id="7db25-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7db25-129">SilentlyContinue</span></span>
- <span data-ttu-id="7db25-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="7db25-130">Stop</span></span>
- <span data-ttu-id="7db25-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="7db25-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db25-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7db25-132">-InformationVariable</span></span>
<span data-ttu-id="7db25-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="7db25-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db25-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="7db25-134">-Pre</span></span>
<span data-ttu-id="7db25-135">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="7db25-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db25-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db25-136">-ResourceGroupName</span></span>
<span data-ttu-id="7db25-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7db25-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db25-138">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7db25-138">-SubscriptionId</span></span>
<span data-ttu-id="7db25-139">Das zu verwendende Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7db25-139">The subscription to use.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7db25-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db25-140">CommonParameters</span></span>
<span data-ttu-id="7db25-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db25-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db25-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7db25-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db25-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7db25-143">INPUTS</span></span>

### <span data-ttu-id="7db25-144">GUID</span><span class="sxs-lookup"><span data-stu-id="7db25-144">Guid</span></span>
<span data-ttu-id="7db25-145">Der Parameter "Abonnement-Nr" akzeptiert den Wert vom Typ "GUID" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7db25-145">Parameter 'SubscriptionId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="7db25-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7db25-146">OUTPUTS</span></span>

### <span data-ttu-id="7db25-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7db25-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7db25-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="7db25-148">NOTES</span></span>

## <span data-ttu-id="7db25-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7db25-149">RELATED LINKS</span></span>
