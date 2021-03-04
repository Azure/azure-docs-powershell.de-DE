---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 1ef17239338319696d08a316648a158039fa63f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930419"
---
# <span data-ttu-id="5d6a1-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="5d6a1-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="5d6a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6a1-103">Ruft einen geheimen Wert des bestimmten benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="5d6a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d6a1-104">SYNTAX</span></span>

### <span data-ttu-id="5d6a1-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d6a1-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d6a1-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="5d6a1-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d6a1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d6a1-107">DESCRIPTION</span></span>
<span data-ttu-id="5d6a1-108">Ruft einen geheimen Wert des bestimmten benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="5d6a1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d6a1-109">EXAMPLES</span></span>

### <span data-ttu-id="5d6a1-110">Beispiel 1: Benannten Wert nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="5d6a1-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="5d6a1-111">Dieser Befehl ruft die benannten Wertdetails mit dem benannten Wertnamen ab.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="5d6a1-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5d6a1-112">PARAMETERS</span></span>

### <span data-ttu-id="5d6a1-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5d6a1-113">-Context</span></span>
<span data-ttu-id="5d6a1-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5d6a1-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-115">This parameter is required.</span></span>

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

### <span data-ttu-id="5d6a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6a1-116">-DefaultProfile</span></span>
<span data-ttu-id="5d6a1-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d6a1-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="5d6a1-118">-NamedValueId</span></span>
<span data-ttu-id="5d6a1-119">Bezeichner eines benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-119">Identifier of a the named value.</span></span>
<span data-ttu-id="5d6a1-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-120">This parameter is required.</span></span>

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

### <span data-ttu-id="5d6a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6a1-121">CommonParameters</span></span>
<span data-ttu-id="5d6a1-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6a1-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d6a1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6a1-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d6a1-124">INPUTS</span></span>

### <span data-ttu-id="5d6a1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5d6a1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5d6a1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5d6a1-126">System.String</span></span>

## <span data-ttu-id="5d6a1-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d6a1-127">OUTPUTS</span></span>

### <span data-ttu-id="5d6a1-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="5d6a1-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="5d6a1-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5d6a1-129">NOTES</span></span>

## <span data-ttu-id="5d6a1-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5d6a1-130">RELATED LINKS</span></span>
