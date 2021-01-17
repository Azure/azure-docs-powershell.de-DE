---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471477"
---
# <span data-ttu-id="ef191-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="ef191-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="ef191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef191-102">SYNOPSIS</span></span>
<span data-ttu-id="ef191-103">Ruft einen geheimen Wert des jeweiligen benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="ef191-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="ef191-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef191-104">SYNTAX</span></span>

### <span data-ttu-id="ef191-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef191-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef191-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="ef191-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef191-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef191-107">DESCRIPTION</span></span>
<span data-ttu-id="ef191-108">Ruft einen geheimen Wert des jeweiligen benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="ef191-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="ef191-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef191-109">EXAMPLES</span></span>

### <span data-ttu-id="ef191-110">Beispiel 1: Get named value by name</span><span class="sxs-lookup"><span data-stu-id="ef191-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="ef191-111">Dieser Befehl ruft die Details des benannten Werts mit dem Namen des benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="ef191-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="ef191-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef191-112">PARAMETERS</span></span>

### <span data-ttu-id="ef191-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ef191-113">-Context</span></span>
<span data-ttu-id="ef191-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ef191-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ef191-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ef191-115">This parameter is required.</span></span>

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

### <span data-ttu-id="ef191-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef191-116">-DefaultProfile</span></span>
<span data-ttu-id="ef191-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef191-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef191-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="ef191-118">-NamedValueId</span></span>
<span data-ttu-id="ef191-119">Bezeichner eines benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="ef191-119">Identifier of a the named value.</span></span>
<span data-ttu-id="ef191-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ef191-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef191-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef191-121">CommonParameters</span></span>
<span data-ttu-id="ef191-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef191-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef191-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef191-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef191-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef191-124">INPUTS</span></span>

### <span data-ttu-id="ef191-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ef191-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ef191-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ef191-126">System.String</span></span>

## <span data-ttu-id="ef191-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef191-127">OUTPUTS</span></span>

### <span data-ttu-id="ef191-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="ef191-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="ef191-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef191-129">NOTES</span></span>

## <span data-ttu-id="ef191-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef191-130">RELATED LINKS</span></span>
