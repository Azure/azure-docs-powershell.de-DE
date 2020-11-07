---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 7542e9621d90ffdb19bb8db679592dd17a216d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662985"
---
# <span data-ttu-id="7f4b4-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7f4b4-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="7f4b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f4b4-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f4b4-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f4b4-103">SYNTAX</span></span>

### <span data-ttu-id="7f4b4-104">Abrufen aller Eigenschaften (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f4b4-104">Get all properties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4b4-105">Abrufen nach Eigenschaftskennung</span><span class="sxs-lookup"><span data-stu-id="7f4b4-105">Get by property ID</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f4b4-106">Suchen von Eigenschaften mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="7f4b4-106">Find properties containing Name</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f4b4-107">Suchen von Eigenschaften nach Kategorie</span><span class="sxs-lookup"><span data-stu-id="7f4b4-107">Find properties by Tag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f4b4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f4b4-108">DESCRIPTION</span></span>

## <span data-ttu-id="7f4b4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f4b4-109">EXAMPLES</span></span>

### <span data-ttu-id="7f4b4-110">1:</span><span class="sxs-lookup"><span data-stu-id="7f4b4-110">1:</span></span>
```
PS C:\> Get-AzureRmApiManagementProperty -Context $Context -Name $PropertyName
```

## <span data-ttu-id="7f4b4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f4b4-111">PARAMETERS</span></span>

### <span data-ttu-id="7f4b4-112">-Context</span><span class="sxs-lookup"><span data-stu-id="7f4b4-112">-Context</span></span>
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

### <span data-ttu-id="7f4b4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7f4b4-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Find properties containing Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4b4-114">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="7f4b4-114">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by property ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4b4-115">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f4b4-115">-Tag</span></span>
<span data-ttu-id="7f4b4-116">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="7f4b4-116">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7f4b4-117">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7f4b4-117">For example:</span></span>

<span data-ttu-id="7f4b4-118">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="7f4b4-118">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: Find properties by Tag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4b4-119">-DefaultProfile</span></span>
<span data-ttu-id="7f4b4-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f4b4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f4b4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4b4-121">CommonParameters</span></span>
<span data-ttu-id="7f4b4-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f4b4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4b4-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f4b4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4b4-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f4b4-124">INPUTS</span></span>

## <span data-ttu-id="7f4b4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f4b4-125">OUTPUTS</span></span>

### <span data-ttu-id="7f4b4-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="7f4b4-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="7f4b4-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7f4b4-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="7f4b4-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f4b4-128">NOTES</span></span>

## <span data-ttu-id="7f4b4-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f4b4-129">RELATED LINKS</span></span>

