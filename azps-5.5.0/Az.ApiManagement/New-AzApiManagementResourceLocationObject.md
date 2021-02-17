---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171804"
---
# <span data-ttu-id="d7f07-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="d7f07-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="d7f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7f07-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f07-103">Erstellen sie einen neuen Vertrag für "Ressourcenspeicherort" (wird in Gateways verwendet).</span><span class="sxs-lookup"><span data-stu-id="d7f07-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="d7f07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7f07-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7f07-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7f07-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f07-106">Das **Cmdlet "New-AzApiManagementResourceLocationObject"** erstellt einen neuen Ressourcenspeicherortvertrag (wird in Gateways verwendet).</span><span class="sxs-lookup"><span data-stu-id="d7f07-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="d7f07-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d7f07-107">EXAMPLES</span></span>

### <span data-ttu-id="d7f07-108">Beispiel 1: Erstellen eines Ressourcenspeicherortvertrags</span><span class="sxs-lookup"><span data-stu-id="d7f07-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="d7f07-109">Mit diesem Befehl wird ein Ressourcenspeicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="d7f07-109">This command creates a resource location.</span></span>

## <span data-ttu-id="d7f07-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7f07-110">PARAMETERS</span></span>

### <span data-ttu-id="d7f07-111">-Ort</span><span class="sxs-lookup"><span data-stu-id="d7f07-111">-City</span></span>
<span data-ttu-id="d7f07-112">Ort.</span><span class="sxs-lookup"><span data-stu-id="d7f07-112">Location City.</span></span>
<span data-ttu-id="d7f07-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d7f07-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="d7f07-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="d7f07-114">-CountryOrRegion</span></span>
<span data-ttu-id="d7f07-115">Land oder Region des Standorts.</span><span class="sxs-lookup"><span data-stu-id="d7f07-115">Location Country or Region.</span></span>
<span data-ttu-id="d7f07-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d7f07-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="d7f07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f07-117">-DefaultProfile</span></span>
<span data-ttu-id="d7f07-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7f07-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7f07-119">-District</span><span class="sxs-lookup"><span data-stu-id="d7f07-119">-District</span></span>
<span data-ttu-id="d7f07-120">Standortbezirk.</span><span class="sxs-lookup"><span data-stu-id="d7f07-120">Location District.</span></span>
<span data-ttu-id="d7f07-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d7f07-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="d7f07-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d7f07-122">-Name</span></span>
<span data-ttu-id="d7f07-123">Standortname.</span><span class="sxs-lookup"><span data-stu-id="d7f07-123">Location Name.</span></span>
<span data-ttu-id="d7f07-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d7f07-124">This parameter is required.</span></span>

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

### <span data-ttu-id="d7f07-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f07-125">CommonParameters</span></span>
<span data-ttu-id="d7f07-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f07-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f07-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7f07-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f07-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d7f07-128">INPUTS</span></span>

### <span data-ttu-id="d7f07-129">Keine</span><span class="sxs-lookup"><span data-stu-id="d7f07-129">None</span></span>

## <span data-ttu-id="d7f07-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d7f07-130">OUTPUTS</span></span>

### <span data-ttu-id="d7f07-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="d7f07-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="d7f07-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d7f07-132">NOTES</span></span>

## <span data-ttu-id="d7f07-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d7f07-133">RELATED LINKS</span></span>
