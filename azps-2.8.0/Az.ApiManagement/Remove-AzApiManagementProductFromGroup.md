---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 51f4caf679cf2440165e1808c152162d1f272d05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658176"
---
# <span data-ttu-id="f1a81-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="f1a81-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="f1a81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1a81-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a81-103">Entfernt ein Produkt aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f1a81-103">Removes a product from a group.</span></span>

## <span data-ttu-id="f1a81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1a81-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1a81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1a81-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a81-106">Das Cmdlet **Remove-AzApiManagementProductFromGroup** entfernt ein Produkt aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f1a81-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="f1a81-107">Mit anderen Worten: Dieses Cmdlet entfernt die Gruppenzuordnung aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="f1a81-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="f1a81-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1a81-108">EXAMPLES</span></span>

### <span data-ttu-id="f1a81-109">Beispiel 1: Entfernen eines Produkts aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="f1a81-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="f1a81-110">Dieser Befehl entfernt ein Produkt aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f1a81-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="f1a81-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1a81-111">PARAMETERS</span></span>

### <span data-ttu-id="f1a81-112">-Context</span><span class="sxs-lookup"><span data-stu-id="f1a81-112">-Context</span></span>
<span data-ttu-id="f1a81-113">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f1a81-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f1a81-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f1a81-114">This parameter is required.</span></span>

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

### <span data-ttu-id="f1a81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a81-115">-DefaultProfile</span></span>
<span data-ttu-id="f1a81-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1a81-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1a81-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="f1a81-117">-GroupId</span></span>
<span data-ttu-id="f1a81-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="f1a81-118">Specifies the group ID.</span></span>
<span data-ttu-id="f1a81-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f1a81-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f1a81-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1a81-120">-PassThru</span></span>
<span data-ttu-id="f1a81-121">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, falls dies erfolgreich ist, oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="f1a81-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="f1a81-122">-ProductID</span><span class="sxs-lookup"><span data-stu-id="f1a81-122">-ProductId</span></span>
<span data-ttu-id="f1a81-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="f1a81-123">Specifies the product ID.</span></span>
<span data-ttu-id="f1a81-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f1a81-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f1a81-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a81-125">CommonParameters</span></span>
<span data-ttu-id="f1a81-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a81-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a81-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1a81-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a81-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1a81-128">INPUTS</span></span>

### <span data-ttu-id="f1a81-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1a81-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1a81-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a81-130">System.String</span></span>

### <span data-ttu-id="f1a81-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f1a81-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1a81-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1a81-132">OUTPUTS</span></span>

### <span data-ttu-id="f1a81-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1a81-133">System.Boolean</span></span>

## <span data-ttu-id="f1a81-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1a81-134">NOTES</span></span>

## <span data-ttu-id="f1a81-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1a81-135">RELATED LINKS</span></span>

[<span data-ttu-id="f1a81-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="f1a81-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


