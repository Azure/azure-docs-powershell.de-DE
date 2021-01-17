---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471478"
---
# <span data-ttu-id="81c2f-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="81c2f-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="81c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="81c2f-103">Ruft eine Liste oder einen bestimmten benannten Wert ab.</span><span class="sxs-lookup"><span data-stu-id="81c2f-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="81c2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81c2f-104">SYNTAX</span></span>

### <span data-ttu-id="81c2f-105">GetAllNamedValues (Standard)</span><span class="sxs-lookup"><span data-stu-id="81c2f-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81c2f-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="81c2f-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81c2f-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="81c2f-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81c2f-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="81c2f-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81c2f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81c2f-109">DESCRIPTION</span></span>
<span data-ttu-id="81c2f-110">Das **Cmdlet "Get-AzApiManagementNamedValue"** ruft eine Liste oder einen bestimmten benannten Wert ab.</span><span class="sxs-lookup"><span data-stu-id="81c2f-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="81c2f-111">Der Wert wird nicht in die Ergebnisdetails einbezogen, wenn der benannte Wert als geheim markiert ist.</span><span class="sxs-lookup"><span data-stu-id="81c2f-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="81c2f-112">Um einen geheimen Wert zu erhalten, verwenden **Sie "Get-AzApiManagementNamedValueSecretValue".**</span><span class="sxs-lookup"><span data-stu-id="81c2f-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="81c2f-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81c2f-113">EXAMPLES</span></span>

### <span data-ttu-id="81c2f-114">Beispiel 1: Benannten Wert nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="81c2f-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="81c2f-115">Dieser Befehl ruft die Details des benannten Werts mit dem Namen des benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="81c2f-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="81c2f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81c2f-116">PARAMETERS</span></span>

### <span data-ttu-id="81c2f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="81c2f-117">-Context</span></span>
<span data-ttu-id="81c2f-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="81c2f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="81c2f-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="81c2f-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81c2f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c2f-120">-DefaultProfile</span></span>
<span data-ttu-id="81c2f-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81c2f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81c2f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="81c2f-122">-Name</span></span>
<span data-ttu-id="81c2f-123">Findet benannte Werte mit Namen, die die Zeichenfolge "Name" enthalten.</span><span class="sxs-lookup"><span data-stu-id="81c2f-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="81c2f-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="81c2f-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c2f-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="81c2f-125">-NamedValueId</span></span>
<span data-ttu-id="81c2f-126">Bezeichner des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="81c2f-126">Identifier of the named value.</span></span>
<span data-ttu-id="81c2f-127">Wenn angegeben, wird versucht, einen benannten Wert nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="81c2f-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="81c2f-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="81c2f-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c2f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="81c2f-129">-Tag</span></span>
<span data-ttu-id="81c2f-130">Findet benannte Werte, die einem Tag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="81c2f-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="81c2f-131">Wenn diese Angabe angegeben wird, werden alle einem Tag zugeordneten Eigenschaften angezeigt.</span><span class="sxs-lookup"><span data-stu-id="81c2f-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="81c2f-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="81c2f-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c2f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c2f-133">CommonParameters</span></span>
<span data-ttu-id="81c2f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81c2f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c2f-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81c2f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c2f-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81c2f-136">INPUTS</span></span>

### <span data-ttu-id="81c2f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="81c2f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="81c2f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="81c2f-138">System.String</span></span>

## <span data-ttu-id="81c2f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81c2f-139">OUTPUTS</span></span>

### <span data-ttu-id="81c2f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="81c2f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="81c2f-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="81c2f-141">NOTES</span></span>

## <span data-ttu-id="81c2f-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="81c2f-142">RELATED LINKS</span></span>
