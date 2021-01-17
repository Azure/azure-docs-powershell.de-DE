---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378845"
---
# <span data-ttu-id="8a3a7-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a3a7-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="8a3a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a3a7-103">Entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-103">Removes an application gateway.</span></span>

## <span data-ttu-id="8a3a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a3a7-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a3a7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a3a7-105">DESCRIPTION</span></span>
<span data-ttu-id="8a3a7-106">Das **Cmdlet "Remove-AzApplicationGateway"** entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="8a3a7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a3a7-107">EXAMPLES</span></span>

### <span data-ttu-id="8a3a7-108">Beispiel 1: Entfernen eines angegebenen Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="8a3a7-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8a3a7-109">Mit diesem Befehl wird das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8a3a7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a3a7-110">PARAMETERS</span></span>

### <span data-ttu-id="8a3a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a3a7-111">-DefaultProfile</span></span>
<span data-ttu-id="8a3a7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a3a7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8a3a7-113">-Force</span></span>
<span data-ttu-id="8a3a7-114">Gibt an, dass das Cmdlet das Löschen des Anwendungsgateways erzwingt, unabhängig davon, ob ihm Ressourcen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="8a3a7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8a3a7-115">-Name</span></span>
<span data-ttu-id="8a3a7-116">Gibt den Namen des Anwendungsgateways an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="8a3a7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a3a7-117">-PassThru</span></span>
<span data-ttu-id="8a3a7-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a3a7-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8a3a7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a3a7-120">-ResourceGroupName</span></span>
<span data-ttu-id="8a3a7-121">Gibt den Namen der Ressourcengruppe an, zu der das Anwendungsgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="8a3a7-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a3a7-122">-Confirm</span></span>
<span data-ttu-id="8a3a7-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a3a7-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8a3a7-124">-WhatIf</span></span>
<span data-ttu-id="8a3a7-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a3a7-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a3a7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a3a7-127">CommonParameters</span></span>
<span data-ttu-id="8a3a7-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a3a7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a3a7-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a3a7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a3a7-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a3a7-130">INPUTS</span></span>

### <span data-ttu-id="8a3a7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8a3a7-131">System.String</span></span>

### <span data-ttu-id="8a3a7-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8a3a7-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8a3a7-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a3a7-133">OUTPUTS</span></span>

### <span data-ttu-id="8a3a7-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a3a7-134">System.Boolean</span></span>

## <span data-ttu-id="8a3a7-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8a3a7-135">NOTES</span></span>

## <span data-ttu-id="8a3a7-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8a3a7-136">RELATED LINKS</span></span>

[<span data-ttu-id="8a3a7-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a3a7-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


