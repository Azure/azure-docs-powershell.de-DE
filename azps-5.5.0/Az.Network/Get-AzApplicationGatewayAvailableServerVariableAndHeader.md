---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157129"
---
# <span data-ttu-id="9804b-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="9804b-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="9804b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9804b-102">SYNOPSIS</span></span>
<span data-ttu-id="9804b-103">Holen Sie sich die unterstützten Servervariablen sowie die verfügbaren Anforderungs- und Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="9804b-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="9804b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9804b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="9804b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9804b-105">DESCRIPTION</span></span>
<span data-ttu-id="9804b-106">Das **Cmdlet "Get-AzApplicationGatewayAvailableServerVariableAndHeader"** ruft die unterstützten Servervariablen sowie die verfügbaren Anforderungs- und Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="9804b-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="9804b-107">Parameter können verwendet werden, um die Variablen oder Headerlisten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9804b-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="9804b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9804b-108">EXAMPLES</span></span>

### <span data-ttu-id="9804b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9804b-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="9804b-110">Diese Befehle geben alle verfügbaren Servervariablen zurück.</span><span class="sxs-lookup"><span data-stu-id="9804b-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="9804b-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9804b-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="9804b-112">Diese Befehle geben alle verfügbaren Anforderungsheader zurück.</span><span class="sxs-lookup"><span data-stu-id="9804b-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="9804b-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9804b-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="9804b-114">Diese Befehle geben alle verfügbaren Antwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="9804b-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="9804b-115">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="9804b-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="9804b-116">Diese Befehle geben alle verfügbaren Servervariablen, Anforderungs- und Antwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="9804b-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="9804b-117">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="9804b-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="9804b-118">Diese Befehle geben alle verfügbaren Servervariablen, Anforderungs- und Antwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="9804b-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="9804b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9804b-119">PARAMETERS</span></span>

### <span data-ttu-id="9804b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9804b-120">-DefaultProfile</span></span>
<span data-ttu-id="9804b-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9804b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9804b-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="9804b-122">-RequestHeader</span></span>
<span data-ttu-id="9804b-123">Verfügbare Anforderungsheader des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="9804b-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="9804b-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="9804b-124">-ResponseHeader</span></span>
<span data-ttu-id="9804b-125">Verfügbare Antwortheader des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="9804b-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="9804b-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="9804b-126">-ServerVariable</span></span>
<span data-ttu-id="9804b-127">Verfügbare Servervariablen des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="9804b-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="9804b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9804b-128">CommonParameters</span></span>
<span data-ttu-id="9804b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9804b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9804b-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9804b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9804b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9804b-131">INPUTS</span></span>

### <span data-ttu-id="9804b-132">Keine</span><span class="sxs-lookup"><span data-stu-id="9804b-132">None</span></span>

## <span data-ttu-id="9804b-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9804b-133">OUTPUTS</span></span>

### <span data-ttu-id="9804b-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="9804b-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="9804b-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9804b-135">NOTES</span></span>
<span data-ttu-id="9804b-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** ist ein Alias für das **Cmdlet "Get-AzApplicationGatewayAvailableServerVariableAndHeader".**</span><span class="sxs-lookup"><span data-stu-id="9804b-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="9804b-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9804b-137">RELATED LINKS</span></span>
