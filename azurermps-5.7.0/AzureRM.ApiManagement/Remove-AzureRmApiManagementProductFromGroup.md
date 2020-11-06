---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: 2eba88e94cfed3c253a5b5febc20a7585ab096d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477050"
---
# <span data-ttu-id="f614a-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="f614a-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="f614a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f614a-102">SYNOPSIS</span></span>
<span data-ttu-id="f614a-103">Entfernt ein Produkt aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f614a-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f614a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f614a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f614a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f614a-105">DESCRIPTION</span></span>
<span data-ttu-id="f614a-106">Das Cmdlet **Remove-AzureRmApiManagementProductFromGroup** entfernt ein Produkt aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f614a-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="f614a-107">Mit anderen Worten: Dieses Cmdlet entfernt die Gruppenzuordnung aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="f614a-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="f614a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f614a-108">EXAMPLES</span></span>

### <span data-ttu-id="f614a-109">Beispiel 1: Entfernen eines Produkts aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="f614a-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="f614a-110">Dieser Befehl entfernt ein Produkt aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f614a-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="f614a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f614a-111">PARAMETERS</span></span>

### <span data-ttu-id="f614a-112">-Context</span><span class="sxs-lookup"><span data-stu-id="f614a-112">-Context</span></span>
<span data-ttu-id="f614a-113">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f614a-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f614a-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f614a-114">This parameter is required.</span></span>

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

### <span data-ttu-id="f614a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f614a-115">-DefaultProfile</span></span>
<span data-ttu-id="f614a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f614a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f614a-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="f614a-117">-GroupId</span></span>
<span data-ttu-id="f614a-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="f614a-118">Specifies the group ID.</span></span>
<span data-ttu-id="f614a-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f614a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f614a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f614a-120">-PassThru</span></span>
<span data-ttu-id="f614a-121">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, falls dies erfolgreich ist, oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="f614a-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="f614a-122">-ProductID</span><span class="sxs-lookup"><span data-stu-id="f614a-122">-ProductId</span></span>
<span data-ttu-id="f614a-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="f614a-123">Specifies the product ID.</span></span>
<span data-ttu-id="f614a-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f614a-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f614a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f614a-125">CommonParameters</span></span>
<span data-ttu-id="f614a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f614a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f614a-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f614a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f614a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f614a-128">INPUTS</span></span>

### <span data-ttu-id="f614a-129">Keine</span><span class="sxs-lookup"><span data-stu-id="f614a-129">None</span></span>
<span data-ttu-id="f614a-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f614a-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f614a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f614a-131">OUTPUTS</span></span>

### <span data-ttu-id="f614a-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f614a-132">System.Boolean</span></span>

## <span data-ttu-id="f614a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f614a-133">NOTES</span></span>

## <span data-ttu-id="f614a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f614a-134">RELATED LINKS</span></span>

[<span data-ttu-id="f614a-135">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="f614a-135">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


