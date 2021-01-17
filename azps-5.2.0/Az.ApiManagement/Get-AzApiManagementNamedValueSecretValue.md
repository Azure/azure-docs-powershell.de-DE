---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365838"
---
# <span data-ttu-id="22cc1-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="22cc1-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="22cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="22cc1-103">Ruft einen geheimen Wert des jeweiligen benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="22cc1-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="22cc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22cc1-104">SYNTAX</span></span>

### <span data-ttu-id="22cc1-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="22cc1-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22cc1-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="22cc1-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22cc1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22cc1-107">DESCRIPTION</span></span>
<span data-ttu-id="22cc1-108">Ruft einen geheimen Wert des jeweiligen benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="22cc1-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="22cc1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22cc1-109">EXAMPLES</span></span>

### <span data-ttu-id="22cc1-110">Beispiel 1: Get named value by name</span><span class="sxs-lookup"><span data-stu-id="22cc1-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="22cc1-111">Dieser Befehl ruft die Details des benannten Werts mit dem Namen des benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="22cc1-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="22cc1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22cc1-112">PARAMETERS</span></span>

### <span data-ttu-id="22cc1-113">-Context</span><span class="sxs-lookup"><span data-stu-id="22cc1-113">-Context</span></span>
<span data-ttu-id="22cc1-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="22cc1-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="22cc1-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="22cc1-115">This parameter is required.</span></span>

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

### <span data-ttu-id="22cc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cc1-116">-DefaultProfile</span></span>
<span data-ttu-id="22cc1-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22cc1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cc1-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="22cc1-118">-NamedValueId</span></span>
<span data-ttu-id="22cc1-119">Bezeichner eines benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="22cc1-119">Identifier of a the named value.</span></span>
<span data-ttu-id="22cc1-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="22cc1-120">This parameter is required.</span></span>

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

### <span data-ttu-id="22cc1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cc1-121">CommonParameters</span></span>
<span data-ttu-id="22cc1-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cc1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cc1-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22cc1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cc1-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22cc1-124">INPUTS</span></span>

### <span data-ttu-id="22cc1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="22cc1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="22cc1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="22cc1-126">System.String</span></span>

## <span data-ttu-id="22cc1-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22cc1-127">OUTPUTS</span></span>

### <span data-ttu-id="22cc1-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="22cc1-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="22cc1-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22cc1-129">NOTES</span></span>

## <span data-ttu-id="22cc1-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22cc1-130">RELATED LINKS</span></span>
