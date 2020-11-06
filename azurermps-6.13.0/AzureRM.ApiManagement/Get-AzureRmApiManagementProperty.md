---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 22cba1b904032ee654b091d1adae541848fd50c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476393"
---
# <span data-ttu-id="a17f6-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="a17f6-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="a17f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a17f6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a17f6-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="a17f6-103">SYNTAX</span></span>

### <span data-ttu-id="a17f6-104">GetAllProperties (Standard)</span><span class="sxs-lookup"><span data-stu-id="a17f6-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a17f6-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="a17f6-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a17f6-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="a17f6-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a17f6-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="a17f6-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a17f6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a17f6-108">DESCRIPTION</span></span>

## <span data-ttu-id="a17f6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a17f6-109">EXAMPLES</span></span>

### <span data-ttu-id="a17f6-110">Beispiel 1: Abrufen einer Eigenschaft nach Name</span><span class="sxs-lookup"><span data-stu-id="a17f6-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="a17f6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a17f6-111">PARAMETERS</span></span>

### <span data-ttu-id="a17f6-112">-Context</span><span class="sxs-lookup"><span data-stu-id="a17f6-112">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a17f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a17f6-113">-DefaultProfile</span></span>
<span data-ttu-id="a17f6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a17f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a17f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a17f6-115">-Name</span></span>
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

### <span data-ttu-id="a17f6-116">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="a17f6-116">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a17f6-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="a17f6-117">-Tag</span></span>
<span data-ttu-id="a17f6-118">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="a17f6-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a17f6-119">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="a17f6-119">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a17f6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a17f6-120">CommonParameters</span></span>
<span data-ttu-id="a17f6-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a17f6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a17f6-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a17f6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a17f6-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a17f6-123">INPUTS</span></span>

### <span data-ttu-id="a17f6-124">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a17f6-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a17f6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a17f6-125">System.String</span></span>

## <span data-ttu-id="a17f6-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a17f6-126">OUTPUTS</span></span>

### <span data-ttu-id="a17f6-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="a17f6-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="a17f6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a17f6-128">NOTES</span></span>

## <span data-ttu-id="a17f6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a17f6-129">RELATED LINKS</span></span>
