---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 791bbe35b480fe9779712d33a37a999bb651a132
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927491"
---
# <span data-ttu-id="a991a-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="a991a-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="a991a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a991a-102">SYNOPSIS</span></span>
<span data-ttu-id="a991a-103">Ruft eine Liste oder einen bestimmten benannten Wert ab.</span><span class="sxs-lookup"><span data-stu-id="a991a-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="a991a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a991a-104">SYNTAX</span></span>

### <span data-ttu-id="a991a-105">GetAllNamedValues (Standard)</span><span class="sxs-lookup"><span data-stu-id="a991a-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a991a-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="a991a-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a991a-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="a991a-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a991a-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="a991a-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a991a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a991a-109">DESCRIPTION</span></span>
<span data-ttu-id="a991a-110">Das **Get-AzApiManagementNamedValue-Cmdlet** ruft eine Liste oder einen bestimmten benannten Wert ab.</span><span class="sxs-lookup"><span data-stu-id="a991a-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="a991a-111">Der Wert wird nicht in die Ergebnisdetails einbezogen, wenn der benannte Wert als geheim gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="a991a-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="a991a-112">Um einen geheimen Wert zu erhalten, verwenden **Sie Get-AzApiManagementNamedValueSecretValue**.</span><span class="sxs-lookup"><span data-stu-id="a991a-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="a991a-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a991a-113">EXAMPLES</span></span>

### <span data-ttu-id="a991a-114">Beispiel 1: Benannten Wert nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="a991a-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="a991a-115">Dieser Befehl ruft die benannten Wertdetails mit dem benannten Wertnamen ab.</span><span class="sxs-lookup"><span data-stu-id="a991a-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="a991a-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a991a-116">PARAMETERS</span></span>

### <span data-ttu-id="a991a-117">-Context</span><span class="sxs-lookup"><span data-stu-id="a991a-117">-Context</span></span>
<span data-ttu-id="a991a-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a991a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a991a-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a991a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="a991a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a991a-120">-DefaultProfile</span></span>
<span data-ttu-id="a991a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a991a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a991a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a991a-122">-Name</span></span>
<span data-ttu-id="a991a-123">Findet benannte Werte mit Namen, die die Zeichenfolge Name enthalten.</span><span class="sxs-lookup"><span data-stu-id="a991a-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="a991a-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a991a-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="a991a-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="a991a-125">-NamedValueId</span></span>
<span data-ttu-id="a991a-126">Bezeichner des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="a991a-126">Identifier of the named value.</span></span>
<span data-ttu-id="a991a-127">Wenn angegeben wird, wird versucht, den benannten Wert durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="a991a-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="a991a-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a991a-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="a991a-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="a991a-129">-Tag</span></span>
<span data-ttu-id="a991a-130">Findet benannte Werte, die einem Tag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a991a-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="a991a-131">Wenn angegeben wird, werden alle Eigenschaften zurück, die einem Tag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a991a-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="a991a-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a991a-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="a991a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a991a-133">CommonParameters</span></span>
<span data-ttu-id="a991a-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a991a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a991a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a991a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a991a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a991a-136">INPUTS</span></span>

### <span data-ttu-id="a991a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a991a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a991a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a991a-138">System.String</span></span>

## <span data-ttu-id="a991a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a991a-139">OUTPUTS</span></span>

### <span data-ttu-id="a991a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="a991a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="a991a-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a991a-141">NOTES</span></span>

## <span data-ttu-id="a991a-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a991a-142">RELATED LINKS</span></span>
