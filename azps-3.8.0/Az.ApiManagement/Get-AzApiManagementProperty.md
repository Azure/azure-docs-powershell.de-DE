---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: a1ca7766efc79d3d9db2d8feef94a2bb7aab9c36
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996624"
---
# <span data-ttu-id="ec7bb-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ec7bb-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="ec7bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7bb-103">Ruft eine Liste oder eine bestimmte Eigenschaft (benannter Wert) ab.</span><span class="sxs-lookup"><span data-stu-id="ec7bb-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="ec7bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec7bb-104">SYNTAX</span></span>

### <span data-ttu-id="ec7bb-105">GetAllProperties (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec7bb-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec7bb-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="ec7bb-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec7bb-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="ec7bb-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec7bb-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="ec7bb-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec7bb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec7bb-109">DESCRIPTION</span></span>
<span data-ttu-id="ec7bb-110">Das Cmdlet " **Get-AzApiManagementProperty** " Ruft eine Liste oder eine bestimmte Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="ec7bb-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="ec7bb-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec7bb-111">EXAMPLES</span></span>

### <span data-ttu-id="ec7bb-112">Beispiel 1: Abrufen einer Eigenschaft nach Name</span><span class="sxs-lookup"><span data-stu-id="ec7bb-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="ec7bb-113">Dieser Befehl ruft die Eigenschaften Details ab, wobei der Eigenschaften Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec7bb-113">This command gets the property details given the property name.</span></span>

## <span data-ttu-id="ec7bb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec7bb-114">PARAMETERS</span></span>

### <span data-ttu-id="ec7bb-115">-Context</span><span class="sxs-lookup"><span data-stu-id="ec7bb-115">-Context</span></span>
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

### <span data-ttu-id="ec7bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7bb-116">-DefaultProfile</span></span>
<span data-ttu-id="ec7bb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec7bb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec7bb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ec7bb-118">-Name</span></span>
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

### <span data-ttu-id="ec7bb-119">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="ec7bb-119">-PropertyId</span></span>
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

### <span data-ttu-id="ec7bb-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec7bb-120">-Tag</span></span>
<span data-ttu-id="ec7bb-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="ec7bb-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ec7bb-122">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="ec7bb-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ec7bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7bb-123">CommonParameters</span></span>
<span data-ttu-id="ec7bb-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec7bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7bb-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec7bb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7bb-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec7bb-126">INPUTS</span></span>

### <span data-ttu-id="ec7bb-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ec7bb-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ec7bb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ec7bb-128">System.String</span></span>

## <span data-ttu-id="ec7bb-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec7bb-129">OUTPUTS</span></span>

### <span data-ttu-id="ec7bb-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ec7bb-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="ec7bb-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec7bb-131">NOTES</span></span>

## <span data-ttu-id="ec7bb-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec7bb-132">RELATED LINKS</span></span>
