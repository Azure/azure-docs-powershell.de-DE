---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008225"
---
# <span data-ttu-id="27d27-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="27d27-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="27d27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27d27-102">SYNOPSIS</span></span>
<span data-ttu-id="27d27-103">Ruft eine Liste oder einen bestimmten benannten Wert ab.</span><span class="sxs-lookup"><span data-stu-id="27d27-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="27d27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27d27-104">SYNTAX</span></span>

### <span data-ttu-id="27d27-105">GetAllNamedValues (Standard)</span><span class="sxs-lookup"><span data-stu-id="27d27-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27d27-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="27d27-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27d27-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="27d27-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27d27-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="27d27-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27d27-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27d27-109">DESCRIPTION</span></span>
<span data-ttu-id="27d27-110">Das Cmdlet " **Get-AzApiManagementNamedValue** " Ruft eine Liste oder einen bestimmten benannten Wert ab.</span><span class="sxs-lookup"><span data-stu-id="27d27-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="27d27-111">Der Wert wird in Ergebnisdetails nicht berücksichtigt, wenn der benannte Wert als geheim gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="27d27-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="27d27-112">Verwenden **Sie Get-AzApiManagementNamedValueSecretValue** , um einen geheimen Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="27d27-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="27d27-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27d27-113">EXAMPLES</span></span>

### <span data-ttu-id="27d27-114">Beispiel 1: Abrufen des benannten Werts nach Name</span><span class="sxs-lookup"><span data-stu-id="27d27-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="27d27-115">Dieser Befehl ruft die Details des benannten Werts ab, wobei der Name des benannten Werts angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="27d27-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="27d27-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="27d27-116">PARAMETERS</span></span>

### <span data-ttu-id="27d27-117">-Context</span><span class="sxs-lookup"><span data-stu-id="27d27-117">-Context</span></span>
<span data-ttu-id="27d27-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="27d27-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="27d27-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="27d27-119">This parameter is required.</span></span>

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

### <span data-ttu-id="27d27-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d27-120">-DefaultProfile</span></span>
<span data-ttu-id="27d27-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27d27-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27d27-122">-Name</span><span class="sxs-lookup"><span data-stu-id="27d27-122">-Name</span></span>
<span data-ttu-id="27d27-123">Findet benannte Werte mit Namen, die den Zeichenfolgennamen enthalten.</span><span class="sxs-lookup"><span data-stu-id="27d27-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="27d27-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="27d27-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="27d27-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="27d27-125">-NamedValueId</span></span>
<span data-ttu-id="27d27-126">Der Bezeichner des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="27d27-126">Identifier of the named value.</span></span>
<span data-ttu-id="27d27-127">Wenn angegeben, wird versucht, den benannten Wert anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="27d27-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="27d27-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="27d27-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="27d27-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="27d27-129">-Tag</span></span>
<span data-ttu-id="27d27-130">Findet benannte Werte, die einem Tag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="27d27-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="27d27-131">Wenn angegeben, werden alle Eigenschaften zurückgegeben, die mit einem Tag verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="27d27-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="27d27-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="27d27-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="27d27-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d27-133">CommonParameters</span></span>
<span data-ttu-id="27d27-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27d27-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d27-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27d27-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d27-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27d27-136">INPUTS</span></span>

### <span data-ttu-id="27d27-137">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="27d27-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="27d27-138">System. String</span><span class="sxs-lookup"><span data-stu-id="27d27-138">System.String</span></span>

## <span data-ttu-id="27d27-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27d27-139">OUTPUTS</span></span>

### <span data-ttu-id="27d27-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="27d27-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="27d27-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="27d27-141">NOTES</span></span>

## <span data-ttu-id="27d27-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27d27-142">RELATED LINKS</span></span>
