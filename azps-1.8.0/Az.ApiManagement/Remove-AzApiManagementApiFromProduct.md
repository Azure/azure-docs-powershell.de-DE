---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: 34631b2f1ac68e5f58c6269fa473dcf3d9103c7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821111"
---
# <span data-ttu-id="63c10-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="63c10-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="63c10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63c10-102">SYNOPSIS</span></span>
<span data-ttu-id="63c10-103">Entfernt eine API aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="63c10-103">Removes an API from a product.</span></span>

## <span data-ttu-id="63c10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63c10-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63c10-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63c10-105">DESCRIPTION</span></span>
<span data-ttu-id="63c10-106">Das Cmdlet **Remove-AzApiManagementApiFromProduct** entfernt eine Azure API-Verwaltungs-API aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="63c10-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="63c10-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63c10-107">EXAMPLES</span></span>

### <span data-ttu-id="63c10-108">Beispiel 1: Entfernen einer API von einem Produkt</span><span class="sxs-lookup"><span data-stu-id="63c10-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="63c10-109">Diese commnd entfernt die angegebene API aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="63c10-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="63c10-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c10-110">PARAMETERS</span></span>

### <span data-ttu-id="63c10-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="63c10-111">-ApiId</span></span>
<span data-ttu-id="63c10-112">Gibt die ID der API an, die aus dem Produkt entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c10-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="63c10-113">-Context</span><span class="sxs-lookup"><span data-stu-id="63c10-113">-Context</span></span>
<span data-ttu-id="63c10-114">Gibt einen **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="63c10-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="63c10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c10-115">-DefaultProfile</span></span>
<span data-ttu-id="63c10-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63c10-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63c10-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63c10-117">-PassThru</span></span>
<span data-ttu-id="63c10-118">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="63c10-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="63c10-119">-ProductID</span><span class="sxs-lookup"><span data-stu-id="63c10-119">-ProductId</span></span>
<span data-ttu-id="63c10-120">Gibt die ID des Produkts an, aus dem die API entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c10-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="63c10-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c10-121">CommonParameters</span></span>
<span data-ttu-id="63c10-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63c10-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c10-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63c10-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c10-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63c10-124">INPUTS</span></span>

### <span data-ttu-id="63c10-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="63c10-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="63c10-126">System. String</span><span class="sxs-lookup"><span data-stu-id="63c10-126">System.String</span></span>

### <span data-ttu-id="63c10-127">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="63c10-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63c10-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63c10-128">OUTPUTS</span></span>

### <span data-ttu-id="63c10-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63c10-129">System.Boolean</span></span>

## <span data-ttu-id="63c10-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="63c10-130">NOTES</span></span>

## <span data-ttu-id="63c10-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63c10-131">RELATED LINKS</span></span>

[<span data-ttu-id="63c10-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="63c10-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


