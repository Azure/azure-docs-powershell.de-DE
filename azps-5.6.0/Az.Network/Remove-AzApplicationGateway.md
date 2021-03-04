---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: 7095190570e649ab5262de0a8cebfc97d55fbf17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934763"
---
# <span data-ttu-id="5a378-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a378-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="5a378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a378-102">SYNOPSIS</span></span>
<span data-ttu-id="5a378-103">Entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5a378-103">Removes an application gateway.</span></span>

## <span data-ttu-id="5a378-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a378-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a378-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a378-105">DESCRIPTION</span></span>
<span data-ttu-id="5a378-106">Das **Cmdlet Remove-AzApplicationGateway** entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5a378-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="5a378-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a378-107">EXAMPLES</span></span>

### <span data-ttu-id="5a378-108">Beispiel 1: Entfernen eines angegebenen Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="5a378-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5a378-109">Mit diesem Befehl wird das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="5a378-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="5a378-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5a378-110">PARAMETERS</span></span>

### <span data-ttu-id="5a378-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a378-111">-DefaultProfile</span></span>
<span data-ttu-id="5a378-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a378-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a378-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="5a378-113">-Force</span></span>
<span data-ttu-id="5a378-114">Gibt an, dass das Cmdlet das Löschen des Anwendungsgateways erzwingt, unabhängig davon, ob ihm Ressourcen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="5a378-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="5a378-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5a378-115">-Name</span></span>
<span data-ttu-id="5a378-116">Gibt den Namen des zu entfernenden Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="5a378-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a378-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a378-117">-PassThru</span></span>
<span data-ttu-id="5a378-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5a378-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a378-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5a378-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a378-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a378-120">-ResourceGroupName</span></span>
<span data-ttu-id="5a378-121">Gibt den Namen des Ressourcengruppennamens an, zu dem das Anwendungsgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="5a378-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="5a378-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a378-122">-Confirm</span></span>
<span data-ttu-id="5a378-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a378-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a378-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a378-124">-WhatIf</span></span>
<span data-ttu-id="5a378-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a378-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a378-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a378-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a378-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a378-127">CommonParameters</span></span>
<span data-ttu-id="5a378-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a378-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a378-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a378-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a378-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a378-130">INPUTS</span></span>

### <span data-ttu-id="5a378-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5a378-131">System.String</span></span>

### <span data-ttu-id="5a378-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a378-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a378-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a378-133">OUTPUTS</span></span>

### <span data-ttu-id="5a378-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a378-134">System.Boolean</span></span>

## <span data-ttu-id="5a378-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5a378-135">NOTES</span></span>

## <span data-ttu-id="5a378-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5a378-136">RELATED LINKS</span></span>

[<span data-ttu-id="5a378-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a378-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


