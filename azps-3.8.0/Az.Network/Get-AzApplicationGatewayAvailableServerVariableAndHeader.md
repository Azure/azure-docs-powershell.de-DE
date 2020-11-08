---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003790"
---
# <span data-ttu-id="d5ef3-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="d5ef3-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="d5ef3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ef3-103">Rufen Sie die unterstützten Servervariablen und verfügbaren Anforderungs-und Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="d5ef3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5ef3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="d5ef3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ef3-106">Das Cmdlet " **Get-AzApplicationGatewayAvailableServerVariableAndHeader** " Ruft die unterstützten Servervariablen und verfügbaren Anforderungs-und Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="d5ef3-107">Parameter können verwendet werden, um die Variablen oder kopfzeilenlisten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="d5ef3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5ef3-108">EXAMPLES</span></span>

### <span data-ttu-id="d5ef3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5ef3-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="d5ef3-110">Diese Befehle gibt alle verfügbaren Servervariablen zurück.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="d5ef3-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d5ef3-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="d5ef3-112">Diese Befehle gibt alle verfügbaren Anforderungsheader zurück.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="d5ef3-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d5ef3-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="d5ef3-114">Diese Befehle gibt alle verfügbaren Antwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="d5ef3-115">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d5ef3-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="d5ef3-116">Diese Befehle gibt alle verfügbaren Servervariablen, Anforderungs-und Antwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="d5ef3-117">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="d5ef3-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="d5ef3-118">Diese Befehle gibt alle verfügbaren Servervariablen, Anforderungs-und Antwortheader zurück.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="d5ef3-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5ef3-119">PARAMETERS</span></span>

### <span data-ttu-id="d5ef3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ef3-120">-DefaultProfile</span></span>
<span data-ttu-id="d5ef3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5ef3-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="d5ef3-122">-RequestHeader</span></span>
<span data-ttu-id="d5ef3-123">Verfügbarer Anforderungsheader für Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="d5ef3-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="d5ef3-124">-ResponseHeader</span></span>
<span data-ttu-id="d5ef3-125">Verfügbare Antwortheader für Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="d5ef3-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="d5ef3-126">-ServerVariable</span></span>
<span data-ttu-id="d5ef3-127">Application Gateway-verfügbare Servervariablen.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="d5ef3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ef3-128">CommonParameters</span></span>
<span data-ttu-id="d5ef3-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ef3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ef3-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5ef3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ef3-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5ef3-131">INPUTS</span></span>

### <span data-ttu-id="d5ef3-132">Keine</span><span class="sxs-lookup"><span data-stu-id="d5ef3-132">None</span></span>

## <span data-ttu-id="d5ef3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5ef3-133">OUTPUTS</span></span>

### <span data-ttu-id="d5ef3-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="d5ef3-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="d5ef3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5ef3-135">NOTES</span></span>
<span data-ttu-id="d5ef3-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** ist ein Alias für das Cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** .</span><span class="sxs-lookup"><span data-stu-id="d5ef3-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="d5ef3-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5ef3-137">RELATED LINKS</span></span>
