---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303237"
---
# <span data-ttu-id="93617-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="93617-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="93617-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93617-102">SYNOPSIS</span></span>
<span data-ttu-id="93617-103">Entfernt ein Produkt aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="93617-103">Removes a product from a group.</span></span>

## <span data-ttu-id="93617-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93617-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93617-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93617-105">DESCRIPTION</span></span>
<span data-ttu-id="93617-106">Das Cmdlet **Remove-AzApiManagementProductFromGroup** entfernt ein Produkt aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="93617-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="93617-107">Mit anderen Worten: Dieses Cmdlet entfernt die Gruppenzuordnung aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="93617-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="93617-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93617-108">EXAMPLES</span></span>

### <span data-ttu-id="93617-109">Beispiel 1: Entfernen eines Produkts aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="93617-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="93617-110">Dieser Befehl entfernt ein Produkt aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="93617-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="93617-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="93617-111">PARAMETERS</span></span>

### <span data-ttu-id="93617-112">-Context</span><span class="sxs-lookup"><span data-stu-id="93617-112">-Context</span></span>
<span data-ttu-id="93617-113">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="93617-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="93617-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="93617-114">This parameter is required.</span></span>

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

### <span data-ttu-id="93617-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93617-115">-DefaultProfile</span></span>
<span data-ttu-id="93617-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93617-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93617-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="93617-117">-GroupId</span></span>
<span data-ttu-id="93617-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="93617-118">Specifies the group ID.</span></span>
<span data-ttu-id="93617-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="93617-119">This parameter is required.</span></span>

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

### <span data-ttu-id="93617-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93617-120">-PassThru</span></span>
<span data-ttu-id="93617-121">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, falls dies erfolgreich ist, oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="93617-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="93617-122">-ProductID</span><span class="sxs-lookup"><span data-stu-id="93617-122">-ProductId</span></span>
<span data-ttu-id="93617-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="93617-123">Specifies the product ID.</span></span>
<span data-ttu-id="93617-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="93617-124">This parameter is required.</span></span>

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

### <span data-ttu-id="93617-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93617-125">CommonParameters</span></span>
<span data-ttu-id="93617-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93617-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93617-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93617-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93617-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93617-128">INPUTS</span></span>

### <span data-ttu-id="93617-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="93617-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="93617-130">System. String</span><span class="sxs-lookup"><span data-stu-id="93617-130">System.String</span></span>

### <span data-ttu-id="93617-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="93617-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93617-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93617-132">OUTPUTS</span></span>

### <span data-ttu-id="93617-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93617-133">System.Boolean</span></span>

## <span data-ttu-id="93617-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="93617-134">NOTES</span></span>

## <span data-ttu-id="93617-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93617-135">RELATED LINKS</span></span>

[<span data-ttu-id="93617-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="93617-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


