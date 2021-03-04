---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 88b2ae64430f73df242d7003baa2c72ec6512dce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923864"
---
# <span data-ttu-id="6ca8f-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="6ca8f-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="6ca8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ca8f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca8f-103">Erstellen Sie einen neuen Vertrag für ressourcenspeicherort (in Gateways verwendet).</span><span class="sxs-lookup"><span data-stu-id="6ca8f-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="6ca8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ca8f-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ca8f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ca8f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca8f-106">Das **Cmdlet New-AzApiManagementResourceLocationObject** erstellt einen neuen Ressourcenspeicherortvertrag (in Gateways verwendet).</span><span class="sxs-lookup"><span data-stu-id="6ca8f-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="6ca8f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ca8f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca8f-108">Beispiel 1: Erstellen eines Ressourcenspeicherortvertrags</span><span class="sxs-lookup"><span data-stu-id="6ca8f-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="6ca8f-109">Mit diesem Befehl wird ein Ressourcenspeicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-109">This command creates a resource location.</span></span>

## <span data-ttu-id="6ca8f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6ca8f-110">PARAMETERS</span></span>

### <span data-ttu-id="6ca8f-111">-Ort</span><span class="sxs-lookup"><span data-stu-id="6ca8f-111">-City</span></span>
<span data-ttu-id="6ca8f-112">Ortsstadt.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-112">Location City.</span></span>
<span data-ttu-id="6ca8f-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="6ca8f-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="6ca8f-114">-CountryOrRegion</span></span>
<span data-ttu-id="6ca8f-115">Standort Land oder Region.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-115">Location Country or Region.</span></span>
<span data-ttu-id="6ca8f-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="6ca8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca8f-117">-DefaultProfile</span></span>
<span data-ttu-id="6ca8f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca8f-119">-District</span><span class="sxs-lookup"><span data-stu-id="6ca8f-119">-District</span></span>
<span data-ttu-id="6ca8f-120">Ortsbezirk.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-120">Location District.</span></span>
<span data-ttu-id="6ca8f-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="6ca8f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6ca8f-122">-Name</span></span>
<span data-ttu-id="6ca8f-123">Ortsname.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-123">Location Name.</span></span>
<span data-ttu-id="6ca8f-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca8f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca8f-125">CommonParameters</span></span>
<span data-ttu-id="6ca8f-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca8f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca8f-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ca8f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca8f-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ca8f-128">INPUTS</span></span>

### <span data-ttu-id="6ca8f-129">Keine</span><span class="sxs-lookup"><span data-stu-id="6ca8f-129">None</span></span>

## <span data-ttu-id="6ca8f-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ca8f-130">OUTPUTS</span></span>

### <span data-ttu-id="6ca8f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="6ca8f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="6ca8f-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6ca8f-132">NOTES</span></span>

## <span data-ttu-id="6ca8f-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6ca8f-133">RELATED LINKS</span></span>
