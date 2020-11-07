---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: adfb6c4e1c10f2e12b4f631e14caa24f978c725e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650417"
---
# <span data-ttu-id="10a8c-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="10a8c-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="10a8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="10a8c-103">Fügt eine API zu einem Produkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="10a8c-103">Adds an API to a product.</span></span>

## <span data-ttu-id="10a8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10a8c-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10a8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="10a8c-106">Das Cmdlet **Add-AzApiManagementApiToProduct** fügt einem Produkt eine Azure API-Verwaltungs-API hinzu.</span><span class="sxs-lookup"><span data-stu-id="10a8c-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="10a8c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10a8c-107">EXAMPLES</span></span>

### <span data-ttu-id="10a8c-108">Beispiel 1: Hinzufügen einer API zu einem Produkt</span><span class="sxs-lookup"><span data-stu-id="10a8c-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="10a8c-109">Mit diesem Befehl wird die angegebene API dem angegebenen Produkt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="10a8c-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="10a8c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10a8c-110">PARAMETERS</span></span>

### <span data-ttu-id="10a8c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="10a8c-111">-ApiId</span></span>
<span data-ttu-id="10a8c-112">Gibt die ID einer API an, die einem Produkt hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10a8c-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a8c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="10a8c-113">-Context</span></span>
<span data-ttu-id="10a8c-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="10a8c-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="10a8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a8c-115">-DefaultProfile</span></span>
<span data-ttu-id="10a8c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10a8c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10a8c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10a8c-117">-PassThru</span></span>
<span data-ttu-id="10a8c-118">passthru</span><span class="sxs-lookup"><span data-stu-id="10a8c-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a8c-119">-ProductID</span><span class="sxs-lookup"><span data-stu-id="10a8c-119">-ProductId</span></span>
<span data-ttu-id="10a8c-120">Gibt die ID des Produkts an, dem die API hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10a8c-120">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a8c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a8c-121">CommonParameters</span></span>
<span data-ttu-id="10a8c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a8c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a8c-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a8c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a8c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10a8c-124">INPUTS</span></span>

### <span data-ttu-id="10a8c-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="10a8c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="10a8c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="10a8c-126">System.String</span></span>

### <span data-ttu-id="10a8c-127">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="10a8c-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10a8c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10a8c-128">OUTPUTS</span></span>

### <span data-ttu-id="10a8c-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10a8c-129">System.Boolean</span></span>

## <span data-ttu-id="10a8c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="10a8c-130">NOTES</span></span>

## <span data-ttu-id="10a8c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10a8c-131">RELATED LINKS</span></span>

[<span data-ttu-id="10a8c-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="10a8c-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


