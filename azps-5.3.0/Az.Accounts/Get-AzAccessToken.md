---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471593"
---
# <span data-ttu-id="70f2d-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="70f2d-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="70f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="70f2d-103">Erhalten Sie das Token für den unformatierte Zugriff.</span><span class="sxs-lookup"><span data-stu-id="70f2d-103">Get raw access token.</span></span> <span data-ttu-id="70f2d-104">Stellen Sie bei Verwendung von "-ResourceUrl" sicher, dass der Wert mit der aktuellen Azure-Umgebung übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="70f2d-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="70f2d-105">Sie können auf den Wert von `(Get-AzContext).Environment` verweisen.</span><span class="sxs-lookup"><span data-stu-id="70f2d-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="70f2d-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70f2d-106">SYNTAX</span></span>

### <span data-ttu-id="70f2d-107">KnownResourceTypeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="70f2d-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70f2d-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="70f2d-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70f2d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70f2d-109">DESCRIPTION</span></span>
<span data-ttu-id="70f2d-110">Zugriffstoken erhalten</span><span class="sxs-lookup"><span data-stu-id="70f2d-110">Get access token</span></span>

## <span data-ttu-id="70f2d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70f2d-111">EXAMPLES</span></span>

### <span data-ttu-id="70f2d-112">Beispiel 1: Token für den unformatierte Zugriff für den ARM erhalten</span><span class="sxs-lookup"><span data-stu-id="70f2d-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="70f2d-113">Zugriffstoken des ResourceManager-Endpunkts für aktuelles Konto erhalten</span><span class="sxs-lookup"><span data-stu-id="70f2d-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="70f2d-114">Beispiel 2: Token für den unformatierte Zugriff für den AAD-Diagrammendpunkt</span><span class="sxs-lookup"><span data-stu-id="70f2d-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="70f2d-115">Zugriffstoken des AAD -Diagrammendpunkts für aktuelles Konto erhalten</span><span class="sxs-lookup"><span data-stu-id="70f2d-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="70f2d-116">Beispiel 3: Token für den unformatierte Zugriff für den AAD-Diagrammendpunkt</span><span class="sxs-lookup"><span data-stu-id="70f2d-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="70f2d-117">Zugriffstoken des AAD -Diagrammendpunkts für aktuelles Konto erhalten</span><span class="sxs-lookup"><span data-stu-id="70f2d-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="70f2d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70f2d-118">PARAMETERS</span></span>

### <span data-ttu-id="70f2d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f2d-119">-DefaultProfile</span></span>
<span data-ttu-id="70f2d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70f2d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70f2d-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="70f2d-121">-ResourceTypeName</span></span>
<span data-ttu-id="70f2d-122">Optionaler Name des Typs "Neuausführen", unterstützte Werte: AadGraph, AnalysisServices, Arm, Nachweis, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="70f2d-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="70f2d-123">Der Standardwert ist "Arm", wenn dieser nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="70f2d-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f2d-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="70f2d-124">-ResourceUrl</span></span>
<span data-ttu-id="70f2d-125">Ressourcen-URL für das Token, für das Sie token anfordern, z. B. ' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="70f2d-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f2d-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="70f2d-126">-TenantId</span></span>
<span data-ttu-id="70f2d-127">Optionale Mandanten-ID. Verwenden Sie die Mandanten-ID des Standardkontexts, wenn dieser nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="70f2d-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="70f2d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f2d-128">CommonParameters</span></span>
<span data-ttu-id="70f2d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f2d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f2d-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70f2d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f2d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70f2d-131">INPUTS</span></span>

### <span data-ttu-id="70f2d-132">Keine</span><span class="sxs-lookup"><span data-stu-id="70f2d-132">None</span></span>

## <span data-ttu-id="70f2d-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70f2d-133">OUTPUTS</span></span>

### <span data-ttu-id="70f2d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="70f2d-134">System.String</span></span>

## <span data-ttu-id="70f2d-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70f2d-135">NOTES</span></span>

## <span data-ttu-id="70f2d-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70f2d-136">RELATED LINKS</span></span>
