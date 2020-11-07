---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: f7c1db6b4ce7c9df63506cdba8b1a206c22ee03e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665214"
---
# <span data-ttu-id="69e2b-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="69e2b-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="69e2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="69e2b-103">Fügt ein Produkt zu einer Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="69e2b-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69e2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69e2b-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69e2b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69e2b-105">DESCRIPTION</span></span>
<span data-ttu-id="69e2b-106">Mit dem Cmdlet **Add-AzureRmApiManagementProductToGroup** wird ein Produkt zu einer vorhandenen Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="69e2b-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="69e2b-107">Anders ausgedrückt, weist dieses Cmdlet einem Produkt eine Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="69e2b-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="69e2b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69e2b-108">EXAMPLES</span></span>

### <span data-ttu-id="69e2b-109">Beispiel 1: Hinzufügen eines Produkts zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="69e2b-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="69e2b-110">Mit diesem Befehl wird ein Produkt zu einer vorhandenen Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="69e2b-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="69e2b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="69e2b-111">PARAMETERS</span></span>

### <span data-ttu-id="69e2b-112">-Context</span><span class="sxs-lookup"><span data-stu-id="69e2b-112">-Context</span></span>
<span data-ttu-id="69e2b-113">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="69e2b-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="69e2b-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="69e2b-114">This parameter is required.</span></span>

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

### <span data-ttu-id="69e2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e2b-115">-DefaultProfile</span></span>
<span data-ttu-id="69e2b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69e2b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="69e2b-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="69e2b-117">-GroupId</span></span>
<span data-ttu-id="69e2b-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="69e2b-118">Specifies the group ID.</span></span>
<span data-ttu-id="69e2b-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="69e2b-119">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69e2b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69e2b-120">-PassThru</span></span>
<span data-ttu-id="69e2b-121">passthru</span><span class="sxs-lookup"><span data-stu-id="69e2b-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69e2b-122">-ProductID</span><span class="sxs-lookup"><span data-stu-id="69e2b-122">-ProductId</span></span>
<span data-ttu-id="69e2b-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="69e2b-123">Specifies the product ID.</span></span>
<span data-ttu-id="69e2b-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="69e2b-124">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69e2b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e2b-125">CommonParameters</span></span>
<span data-ttu-id="69e2b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69e2b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e2b-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69e2b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e2b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69e2b-128">INPUTS</span></span>

### <span data-ttu-id="69e2b-129">Keine</span><span class="sxs-lookup"><span data-stu-id="69e2b-129">None</span></span>
<span data-ttu-id="69e2b-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="69e2b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69e2b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69e2b-131">OUTPUTS</span></span>

### <span data-ttu-id="69e2b-132">Boolean</span><span class="sxs-lookup"><span data-stu-id="69e2b-132">Boolean</span></span>

## <span data-ttu-id="69e2b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="69e2b-133">NOTES</span></span>

## <span data-ttu-id="69e2b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69e2b-134">RELATED LINKS</span></span>

[<span data-ttu-id="69e2b-135">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="69e2b-135">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


