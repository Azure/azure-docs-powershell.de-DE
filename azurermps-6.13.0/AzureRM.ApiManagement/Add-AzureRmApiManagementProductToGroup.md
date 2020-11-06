---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: 1bd1027c0d58f1ee38ca23c28b3021bdc2b95d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478074"
---
# <span data-ttu-id="c3a01-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="c3a01-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="c3a01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3a01-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a01-103">Fügt ein Produkt zu einer Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="c3a01-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3a01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3a01-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3a01-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3a01-105">DESCRIPTION</span></span>
<span data-ttu-id="c3a01-106">Mit dem Cmdlet **Add-AzureRmApiManagementProductToGroup** wird ein Produkt zu einer vorhandenen Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c3a01-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="c3a01-107">Anders ausgedrückt, weist dieses Cmdlet einem Produkt eine Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="c3a01-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="c3a01-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3a01-108">EXAMPLES</span></span>

### <span data-ttu-id="c3a01-109">Beispiel 1: Hinzufügen eines Produkts zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="c3a01-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="c3a01-110">Mit diesem Befehl wird ein Produkt zu einer vorhandenen Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c3a01-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="c3a01-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3a01-111">PARAMETERS</span></span>

### <span data-ttu-id="c3a01-112">-Context</span><span class="sxs-lookup"><span data-stu-id="c3a01-112">-Context</span></span>
<span data-ttu-id="c3a01-113">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c3a01-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c3a01-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3a01-114">This parameter is required.</span></span>

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

### <span data-ttu-id="c3a01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a01-115">-DefaultProfile</span></span>
<span data-ttu-id="c3a01-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3a01-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3a01-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="c3a01-117">-GroupId</span></span>
<span data-ttu-id="c3a01-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="c3a01-118">Specifies the group ID.</span></span>
<span data-ttu-id="c3a01-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3a01-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c3a01-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3a01-120">-PassThru</span></span>
<span data-ttu-id="c3a01-121">passthru</span><span class="sxs-lookup"><span data-stu-id="c3a01-121">passthru</span></span>

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

### <span data-ttu-id="c3a01-122">-ProductID</span><span class="sxs-lookup"><span data-stu-id="c3a01-122">-ProductId</span></span>
<span data-ttu-id="c3a01-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="c3a01-123">Specifies the product ID.</span></span>
<span data-ttu-id="c3a01-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3a01-124">This parameter is required.</span></span>

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

### <span data-ttu-id="c3a01-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a01-125">CommonParameters</span></span>
<span data-ttu-id="c3a01-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3a01-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a01-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3a01-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a01-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3a01-128">INPUTS</span></span>

### <span data-ttu-id="c3a01-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c3a01-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c3a01-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c3a01-130">System.String</span></span>

### <span data-ttu-id="c3a01-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="c3a01-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c3a01-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3a01-132">OUTPUTS</span></span>

### <span data-ttu-id="c3a01-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3a01-133">System.Boolean</span></span>

## <span data-ttu-id="c3a01-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3a01-134">NOTES</span></span>

## <span data-ttu-id="c3a01-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3a01-135">RELATED LINKS</span></span>

[<span data-ttu-id="c3a01-136">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="c3a01-136">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


