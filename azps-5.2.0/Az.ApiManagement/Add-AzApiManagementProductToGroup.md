---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293927"
---
# <span data-ttu-id="37c2c-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="37c2c-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="37c2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="37c2c-103">Fügt einer Gruppe ein Produkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="37c2c-103">Adds a product to a group.</span></span>

## <span data-ttu-id="37c2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37c2c-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37c2c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37c2c-105">DESCRIPTION</span></span>
<span data-ttu-id="37c2c-106">Das **Cmdlet "Add-AzApiManagementProductToGroup"** fügt einer vorhandenen Gruppe ein Produkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="37c2c-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="37c2c-107">Mit anderen Worten: Dieses Cmdlet weist einem Produkt eine Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="37c2c-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="37c2c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37c2c-108">EXAMPLES</span></span>

### <span data-ttu-id="37c2c-109">Beispiel 1: Hinzufügen eines Produkts zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="37c2c-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="37c2c-110">Mit diesem Befehl wird einer vorhandenen Gruppe ein Produkt hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="37c2c-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="37c2c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37c2c-111">PARAMETERS</span></span>

### <span data-ttu-id="37c2c-112">-Context</span><span class="sxs-lookup"><span data-stu-id="37c2c-112">-Context</span></span>
<span data-ttu-id="37c2c-113">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="37c2c-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="37c2c-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37c2c-114">This parameter is required.</span></span>

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

### <span data-ttu-id="37c2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c2c-115">-DefaultProfile</span></span>
<span data-ttu-id="37c2c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37c2c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37c2c-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="37c2c-117">-GroupId</span></span>
<span data-ttu-id="37c2c-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="37c2c-118">Specifies the group ID.</span></span>
<span data-ttu-id="37c2c-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37c2c-119">This parameter is required.</span></span>

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

### <span data-ttu-id="37c2c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37c2c-120">-PassThru</span></span>
<span data-ttu-id="37c2c-121">passthru</span><span class="sxs-lookup"><span data-stu-id="37c2c-121">passthru</span></span>

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

### <span data-ttu-id="37c2c-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="37c2c-122">-ProductId</span></span>
<span data-ttu-id="37c2c-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="37c2c-123">Specifies the product ID.</span></span>
<span data-ttu-id="37c2c-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37c2c-124">This parameter is required.</span></span>

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

### <span data-ttu-id="37c2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c2c-125">CommonParameters</span></span>
<span data-ttu-id="37c2c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c2c-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37c2c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c2c-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37c2c-128">INPUTS</span></span>

### <span data-ttu-id="37c2c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="37c2c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="37c2c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="37c2c-130">System.String</span></span>

### <span data-ttu-id="37c2c-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="37c2c-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="37c2c-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37c2c-132">OUTPUTS</span></span>

### <span data-ttu-id="37c2c-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37c2c-133">System.Boolean</span></span>

## <span data-ttu-id="37c2c-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37c2c-134">NOTES</span></span>

## <span data-ttu-id="37c2c-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37c2c-135">RELATED LINKS</span></span>

[<span data-ttu-id="37c2c-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="37c2c-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


