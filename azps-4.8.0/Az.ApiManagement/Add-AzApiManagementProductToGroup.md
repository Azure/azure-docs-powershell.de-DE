---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010332"
---
# <span data-ttu-id="b4dda-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="b4dda-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="b4dda-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4dda-102">SYNOPSIS</span></span>
<span data-ttu-id="b4dda-103">Fügt ein Produkt zu einer Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="b4dda-103">Adds a product to a group.</span></span>

## <span data-ttu-id="b4dda-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4dda-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4dda-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4dda-105">DESCRIPTION</span></span>
<span data-ttu-id="b4dda-106">Mit dem Cmdlet **Add-AzApiManagementProductToGroup** wird ein Produkt zu einer vorhandenen Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b4dda-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="b4dda-107">Anders ausgedrückt, weist dieses Cmdlet einem Produkt eine Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="b4dda-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="b4dda-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4dda-108">EXAMPLES</span></span>

### <span data-ttu-id="b4dda-109">Beispiel 1: Hinzufügen eines Produkts zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="b4dda-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="b4dda-110">Mit diesem Befehl wird ein Produkt zu einer vorhandenen Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b4dda-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="b4dda-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4dda-111">PARAMETERS</span></span>

### <span data-ttu-id="b4dda-112">-Context</span><span class="sxs-lookup"><span data-stu-id="b4dda-112">-Context</span></span>
<span data-ttu-id="b4dda-113">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b4dda-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="b4dda-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b4dda-114">This parameter is required.</span></span>

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

### <span data-ttu-id="b4dda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4dda-115">-DefaultProfile</span></span>
<span data-ttu-id="b4dda-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4dda-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4dda-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="b4dda-117">-GroupId</span></span>
<span data-ttu-id="b4dda-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="b4dda-118">Specifies the group ID.</span></span>
<span data-ttu-id="b4dda-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b4dda-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b4dda-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4dda-120">-PassThru</span></span>
<span data-ttu-id="b4dda-121">passthru</span><span class="sxs-lookup"><span data-stu-id="b4dda-121">passthru</span></span>

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

### <span data-ttu-id="b4dda-122">-ProductID</span><span class="sxs-lookup"><span data-stu-id="b4dda-122">-ProductId</span></span>
<span data-ttu-id="b4dda-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="b4dda-123">Specifies the product ID.</span></span>
<span data-ttu-id="b4dda-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b4dda-124">This parameter is required.</span></span>

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

### <span data-ttu-id="b4dda-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4dda-125">CommonParameters</span></span>
<span data-ttu-id="b4dda-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4dda-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4dda-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4dda-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4dda-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4dda-128">INPUTS</span></span>

### <span data-ttu-id="b4dda-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b4dda-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b4dda-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b4dda-130">System.String</span></span>

### <span data-ttu-id="b4dda-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="b4dda-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b4dda-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4dda-132">OUTPUTS</span></span>

### <span data-ttu-id="b4dda-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4dda-133">System.Boolean</span></span>

## <span data-ttu-id="b4dda-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4dda-134">NOTES</span></span>

## <span data-ttu-id="b4dda-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4dda-135">RELATED LINKS</span></span>

[<span data-ttu-id="b4dda-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="b4dda-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


