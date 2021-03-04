---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: f4f2e76a9354ee6ed796b64cbdd83f21d70ff954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931808"
---
# <span data-ttu-id="d7d80-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="d7d80-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="d7d80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7d80-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d80-103">Holen Sie sich die unterstützten Servervariablen sowie verfügbare Anforderungs- und Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="d7d80-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="d7d80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7d80-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="d7d80-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7d80-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d80-106">Das **Get-AzApplicationGatewayAvailableServerVariableAndHeader-Cmdlet** ruft die unterstützten Servervariablen sowie verfügbare Anforderungs- und Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="d7d80-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="d7d80-107">Parameter können verwendet werden, um die Variablen- oder Kopfzeilenlisten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d7d80-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="d7d80-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d7d80-108">EXAMPLES</span></span>

### <span data-ttu-id="d7d80-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d7d80-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="d7d80-110">Diese Befehle geben alle verfügbaren Servervariablen zurück.</span><span class="sxs-lookup"><span data-stu-id="d7d80-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="d7d80-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d7d80-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="d7d80-112">Diese Befehle geben alle verfügbaren Anforderungsüberschriften zurück.</span><span class="sxs-lookup"><span data-stu-id="d7d80-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="d7d80-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d7d80-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="d7d80-114">Diese Befehle geben alle verfügbaren Antwortkopfzeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="d7d80-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="d7d80-115">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d7d80-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="d7d80-116">Diese Befehle geben alle verfügbaren Servervariablen, Anforderungs- und Antwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="d7d80-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="d7d80-117">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="d7d80-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="d7d80-118">Diese Befehle geben alle verfügbaren Servervariablen, Anforderungs- und Antwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="d7d80-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="d7d80-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d7d80-119">PARAMETERS</span></span>

### <span data-ttu-id="d7d80-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d80-120">-DefaultProfile</span></span>
<span data-ttu-id="d7d80-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7d80-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7d80-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="d7d80-122">-RequestHeader</span></span>
<span data-ttu-id="d7d80-123">Verfügbare Anforderungsheader für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d7d80-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="d7d80-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="d7d80-124">-ResponseHeader</span></span>
<span data-ttu-id="d7d80-125">Verfügbare Antwortheader für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d7d80-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="d7d80-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="d7d80-126">-ServerVariable</span></span>
<span data-ttu-id="d7d80-127">Verfügbare Servervariablen für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d7d80-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="d7d80-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d80-128">CommonParameters</span></span>
<span data-ttu-id="d7d80-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d80-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d80-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7d80-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d80-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d7d80-131">INPUTS</span></span>

### <span data-ttu-id="d7d80-132">Keine</span><span class="sxs-lookup"><span data-stu-id="d7d80-132">None</span></span>

## <span data-ttu-id="d7d80-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d7d80-133">OUTPUTS</span></span>

### <span data-ttu-id="d7d80-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="d7d80-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="d7d80-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d7d80-135">NOTES</span></span>
<span data-ttu-id="d7d80-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** ist ein Alias für das **Get-AzApplicationGatewayAvailableServerVariableAndHeader-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="d7d80-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="d7d80-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d7d80-137">RELATED LINKS</span></span>
