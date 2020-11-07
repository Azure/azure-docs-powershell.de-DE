---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: ba7bda62d0d001f11ff729ca0ecce6327b659855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821447"
---
# <span data-ttu-id="0efd6-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0efd6-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="0efd6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0efd6-102">SYNOPSIS</span></span>
<span data-ttu-id="0efd6-103">Entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="0efd6-103">Removes an application gateway.</span></span>

## <span data-ttu-id="0efd6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0efd6-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0efd6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0efd6-105">DESCRIPTION</span></span>
<span data-ttu-id="0efd6-106">Das Cmdlet **Remove-AzApplicationGateway** entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="0efd6-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="0efd6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0efd6-107">EXAMPLES</span></span>

### <span data-ttu-id="0efd6-108">Beispiel 1: Entfernen eines angegebenen Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="0efd6-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0efd6-109">Dieser Befehl entfernt das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0efd6-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0efd6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0efd6-110">PARAMETERS</span></span>

### <span data-ttu-id="0efd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efd6-111">-DefaultProfile</span></span>
<span data-ttu-id="0efd6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0efd6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0efd6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0efd6-113">-Force</span></span>
<span data-ttu-id="0efd6-114">Gibt an, dass das Cmdlet das Löschen des Anwendungs Gateways erzwingt, unabhängig davon, ob ihm Ressourcen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="0efd6-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="0efd6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0efd6-115">-Name</span></span>
<span data-ttu-id="0efd6-116">Gibt den Namen des Anwendungs Gateways an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0efd6-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="0efd6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0efd6-117">-PassThru</span></span>
<span data-ttu-id="0efd6-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0efd6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0efd6-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0efd6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0efd6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efd6-120">-ResourceGroupName</span></span>
<span data-ttu-id="0efd6-121">Gibt den Namen des Ressourcengruppen namens an, zu dem das Anwendungsgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="0efd6-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="0efd6-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0efd6-122">-Confirm</span></span>
<span data-ttu-id="0efd6-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0efd6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efd6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efd6-124">-WhatIf</span></span>
<span data-ttu-id="0efd6-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0efd6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0efd6-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0efd6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efd6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efd6-127">CommonParameters</span></span>
<span data-ttu-id="0efd6-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efd6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efd6-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0efd6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efd6-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0efd6-130">INPUTS</span></span>

### <span data-ttu-id="0efd6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0efd6-131">System.String</span></span>

### <span data-ttu-id="0efd6-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="0efd6-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0efd6-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0efd6-133">OUTPUTS</span></span>

### <span data-ttu-id="0efd6-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0efd6-134">System.Boolean</span></span>

## <span data-ttu-id="0efd6-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="0efd6-135">NOTES</span></span>

## <span data-ttu-id="0efd6-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0efd6-136">RELATED LINKS</span></span>

[<span data-ttu-id="0efd6-137">Satz-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0efd6-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


