---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 06056bd8bf9060a7610b74b8332ff5ab2a4790f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929379"
---
# <span data-ttu-id="6e266-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6e266-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="6e266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e266-102">SYNOPSIS</span></span>
<span data-ttu-id="6e266-103">Ruft den Bereitstellungsvorgang der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6e266-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="6e266-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e266-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e266-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e266-105">DESCRIPTION</span></span>
<span data-ttu-id="6e266-106">Das **Cmdlet Get-AzResourceGroupDeploymentOperation** listet alle Vorgänge auf, die Teil einer Bereitstellung waren, um Ihnen zu helfen, die genauen Vorgänge zu identifizieren und zu geben, die bei einer bestimmten Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="6e266-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="6e266-107">Sie kann auch die Antwort und den Anforderungsinhalt für jeden Bereitstellungsvorgang anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6e266-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="6e266-108">Dies sind dieselben Informationen, die in den Bereitstellungsdetails auf dem Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e266-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="6e266-109">Um die Anforderung und den Antwortinhalt zu erhalten, aktivieren Sie die Einstellung beim Übermitteln einer Bereitstellung über **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="6e266-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="6e266-110">Sie kann potenziell Geheime wie Kennwörter protokollieren und verfügbar machen, die in der Ressourceneigenschaft verwendet werden, oder listKeys-Vorgänge, die beim Abrufen der **Bereitstellungsvorgänge** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e266-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="6e266-111">Weitere Informationen zu dieser Einstellung und deren Aktivierung finden Sie unter New-AzResourceGroupDeployment und Debuggen ARM Vorlagenbereitstellungen.</span><span class="sxs-lookup"><span data-stu-id="6e266-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="6e266-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e266-112">EXAMPLES</span></span>

### <span data-ttu-id="6e266-113">Beispiel 1: Get1</span><span class="sxs-lookup"><span data-stu-id="6e266-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="6e266-114">Ruft den Bereitstellungsvorgang mit dem Namen "Test" unter "Test" der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6e266-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="6e266-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6e266-115">PARAMETERS</span></span>

### <span data-ttu-id="6e266-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e266-116">-DefaultProfile</span></span>
<span data-ttu-id="6e266-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e266-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e266-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="6e266-118">-DeploymentName</span></span>
<span data-ttu-id="6e266-119">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="6e266-119">The deployment name.</span></span>

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

### <span data-ttu-id="6e266-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e266-120">-Pre</span></span>
<span data-ttu-id="6e266-121">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e266-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6e266-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e266-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e266-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e266-123">The resource group name.</span></span>

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

### <span data-ttu-id="6e266-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e266-124">-SubscriptionId</span></span>
<span data-ttu-id="6e266-125">Das zu verwendende Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e266-125">The subscription to use.</span></span>

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

### <span data-ttu-id="6e266-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e266-126">CommonParameters</span></span>
<span data-ttu-id="6e266-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e266-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e266-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e266-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e266-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e266-129">INPUTS</span></span>

### <span data-ttu-id="6e266-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6e266-130">System.String</span></span>

### <span data-ttu-id="6e266-131">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6e266-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6e266-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e266-132">OUTPUTS</span></span>

### <span data-ttu-id="6e266-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6e266-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="6e266-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6e266-134">NOTES</span></span>

## <span data-ttu-id="6e266-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6e266-135">RELATED LINKS</span></span>
