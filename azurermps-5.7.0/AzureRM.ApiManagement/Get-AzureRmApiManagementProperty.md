---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 47167e0729ab3476c74124e16d6ae95901f57ad2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483213"
---
# <span data-ttu-id="8a2e7-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8a2e7-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="8a2e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a2e7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a2e7-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a2e7-103">SYNTAX</span></span>

### <span data-ttu-id="8a2e7-104">GetAllProperties (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a2e7-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a2e7-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="8a2e7-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a2e7-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="8a2e7-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a2e7-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="8a2e7-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a2e7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a2e7-108">DESCRIPTION</span></span>

## <span data-ttu-id="8a2e7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a2e7-109">EXAMPLES</span></span>

### <span data-ttu-id="8a2e7-110">Beispiel 1: Abrufen einer Eigenschaft nach Name</span><span class="sxs-lookup"><span data-stu-id="8a2e7-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="8a2e7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a2e7-111">PARAMETERS</span></span>

### <span data-ttu-id="8a2e7-112">-Context</span><span class="sxs-lookup"><span data-stu-id="8a2e7-112">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2e7-113">-DefaultProfile</span></span>
<span data-ttu-id="8a2e7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2e7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8a2e7-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2e7-116">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="8a2e7-116">-PropertyId</span></span>
```yaml
Type: String
Parameter Sets: GetByPropertyId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2e7-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a2e7-117">-Tag</span></span>
<span data-ttu-id="8a2e7-118">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="8a2e7-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8a2e7-119">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8a2e7-119">For example:</span></span>

<span data-ttu-id="8a2e7-120">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="8a2e7-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: String
Parameter Sets: GetByTag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2e7-121">CommonParameters</span></span>
<span data-ttu-id="8a2e7-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2e7-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a2e7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2e7-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a2e7-124">INPUTS</span></span>

### <span data-ttu-id="8a2e7-125">Keine</span><span class="sxs-lookup"><span data-stu-id="8a2e7-125">None</span></span>
<span data-ttu-id="8a2e7-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8a2e7-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a2e7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a2e7-127">OUTPUTS</span></span>

### <span data-ttu-id="8a2e7-128">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="8a2e7-128">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="8a2e7-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8a2e7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="8a2e7-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a2e7-130">NOTES</span></span>

## <span data-ttu-id="8a2e7-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a2e7-131">RELATED LINKS</span></span>

