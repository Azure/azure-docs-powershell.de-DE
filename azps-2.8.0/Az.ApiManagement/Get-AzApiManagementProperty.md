---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: 2c8fc24d252fce12e7adf9ee824db0e1b2c8b206
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658304"
---
# <span data-ttu-id="8d5c6-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8d5c6-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="8d5c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5c6-103">Ruft eine Liste oder eine bestimmte Eigenschaft (benannter Wert) ab.</span><span class="sxs-lookup"><span data-stu-id="8d5c6-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="8d5c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d5c6-104">SYNTAX</span></span>

### <span data-ttu-id="8d5c6-105">GetAllProperties (Standard)</span><span class="sxs-lookup"><span data-stu-id="8d5c6-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d5c6-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="8d5c6-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d5c6-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="8d5c6-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d5c6-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="8d5c6-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d5c6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d5c6-109">DESCRIPTION</span></span>
<span data-ttu-id="8d5c6-110">Das Cmdlet " **Get-AzApiManagementProperty** " Ruft eine Liste oder eine bestimmte Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="8d5c6-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="8d5c6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d5c6-111">EXAMPLES</span></span>

### <span data-ttu-id="8d5c6-112">Beispiel 1: Abrufen einer Eigenschaft nach Name</span><span class="sxs-lookup"><span data-stu-id="8d5c6-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="8d5c6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d5c6-113">PARAMETERS</span></span>

### <span data-ttu-id="8d5c6-114">-Context</span><span class="sxs-lookup"><span data-stu-id="8d5c6-114">-Context</span></span>
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

### <span data-ttu-id="8d5c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5c6-115">-DefaultProfile</span></span>
<span data-ttu-id="8d5c6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d5c6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d5c6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8d5c6-117">-Name</span></span>
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

### <span data-ttu-id="8d5c6-118">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="8d5c6-118">-PropertyId</span></span>
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

### <span data-ttu-id="8d5c6-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="8d5c6-119">-Tag</span></span>
<span data-ttu-id="8d5c6-120">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="8d5c6-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8d5c6-121">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="8d5c6-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8d5c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5c6-122">CommonParameters</span></span>
<span data-ttu-id="8d5c6-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5c6-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d5c6-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5c6-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d5c6-125">INPUTS</span></span>

### <span data-ttu-id="8d5c6-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d5c6-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d5c6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8d5c6-127">System.String</span></span>

## <span data-ttu-id="8d5c6-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d5c6-128">OUTPUTS</span></span>

### <span data-ttu-id="8d5c6-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8d5c6-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="8d5c6-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d5c6-130">NOTES</span></span>

## <span data-ttu-id="8d5c6-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d5c6-131">RELATED LINKS</span></span>
