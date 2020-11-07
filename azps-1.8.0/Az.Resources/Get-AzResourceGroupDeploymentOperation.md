---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: a67bfb43aa4cafe4b9c7f20e6ff757989deee5d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659629"
---
# <span data-ttu-id="8ee15-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8ee15-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="8ee15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ee15-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee15-103">Ruft den Bereitstellungsvorgang der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8ee15-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="8ee15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ee15-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ee15-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ee15-105">DESCRIPTION</span></span>
<span data-ttu-id="8ee15-106">Das Cmdlet " **Get-AzResourceGroupDeploymentOperation** " listet alle Vorgänge auf, die Teil einer Bereitstellung waren, damit Sie weitere Informationen zu den exakten Vorgängen finden können, die für eine bestimmte Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="8ee15-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="8ee15-107">Außerdem kann die Antwort und der Anforderungs Inhalt für jeden Bereitstellungsvorgang angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ee15-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="8ee15-108">Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8ee15-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="8ee15-109">Um die Anforderung und den Antwortinhalt abzurufen, aktivieren Sie diese Einstellung, wenn Sie eine Bereitstellung über **New-AzResourceGroupDeployment** übermitteln.</span><span class="sxs-lookup"><span data-stu-id="8ee15-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="8ee15-110">Sie kann potenziell Geheimnisse wie Kennwörter protokollieren und verfügbar machen, die in den Ressourceneigenschaften-oder **listKeys** -Vorgängen verwendet werden, die beim Abrufen der Bereitstellungsvorgänge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8ee15-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="8ee15-111">Weitere Informationen zu dieser Einstellung und dazu, wie Sie Sie aktivieren, finden Sie unter New-AzResourceGroupDeployment und Debuggen von Arm-Vorlagen Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="8ee15-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="8ee15-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ee15-112">EXAMPLES</span></span>

### <span data-ttu-id="8ee15-113">Get1</span><span class="sxs-lookup"><span data-stu-id="8ee15-113">Get1</span></span>
```
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="8ee15-114">Ruft den Bereitstellungsvorgang mit dem Namen "Test" unter Ressourcengruppe "Test" ab</span><span class="sxs-lookup"><span data-stu-id="8ee15-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="8ee15-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ee15-115">PARAMETERS</span></span>

### <span data-ttu-id="8ee15-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8ee15-116">-ApiVersion</span></span>
<span data-ttu-id="8ee15-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8ee15-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8ee15-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8ee15-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8ee15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee15-119">-DefaultProfile</span></span>
<span data-ttu-id="8ee15-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8ee15-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ee15-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="8ee15-121">-DeploymentName</span></span>
<span data-ttu-id="8ee15-122">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="8ee15-122">The deployment name.</span></span>

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

### <span data-ttu-id="8ee15-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="8ee15-123">-Pre</span></span>
<span data-ttu-id="8ee15-124">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="8ee15-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8ee15-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee15-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ee15-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8ee15-126">The resource group name.</span></span>

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

### <span data-ttu-id="8ee15-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8ee15-127">-SubscriptionId</span></span>
<span data-ttu-id="8ee15-128">Das zu verwendende Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ee15-128">The subscription to use.</span></span>

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

### <span data-ttu-id="8ee15-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee15-129">CommonParameters</span></span>
<span data-ttu-id="8ee15-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee15-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee15-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ee15-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee15-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ee15-132">INPUTS</span></span>

### <span data-ttu-id="8ee15-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8ee15-133">System.String</span></span>

### <span data-ttu-id="8ee15-134">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ee15-134">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8ee15-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ee15-135">OUTPUTS</span></span>

### <span data-ttu-id="8ee15-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8ee15-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8ee15-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ee15-137">NOTES</span></span>

## <span data-ttu-id="8ee15-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ee15-138">RELATED LINKS</span></span>
