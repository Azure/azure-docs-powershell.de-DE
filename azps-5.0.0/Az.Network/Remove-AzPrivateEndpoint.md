---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303639"
---
# <span data-ttu-id="26e06-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="26e06-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="26e06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26e06-102">SYNOPSIS</span></span>
<span data-ttu-id="26e06-103">Entfernt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="26e06-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="26e06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26e06-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e06-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26e06-105">DESCRIPTION</span></span>
<span data-ttu-id="26e06-106">Mit dem Cmdlet **Remove-AzPrivateEndpoint** wird ein privater Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="26e06-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="26e06-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26e06-107">EXAMPLES</span></span>

### <span data-ttu-id="26e06-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="26e06-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="26e06-109">In diesem Beispiel wird ein privater Endpunkt mit dem Namen MyPrivateEndpoint1 entfernt.</span><span class="sxs-lookup"><span data-stu-id="26e06-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="26e06-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="26e06-110">PARAMETERS</span></span>

### <span data-ttu-id="26e06-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26e06-111">-AsJob</span></span>
<span data-ttu-id="26e06-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="26e06-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26e06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e06-113">-DefaultProfile</span></span>
<span data-ttu-id="26e06-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26e06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e06-115">-Force</span><span class="sxs-lookup"><span data-stu-id="26e06-115">-Force</span></span>
<span data-ttu-id="26e06-116">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="26e06-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="26e06-117">-Name</span><span class="sxs-lookup"><span data-stu-id="26e06-117">-Name</span></span>
<span data-ttu-id="26e06-118">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="26e06-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="26e06-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26e06-119">-PassThru</span></span>
<span data-ttu-id="26e06-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="26e06-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="26e06-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="26e06-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26e06-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e06-122">-ResourceGroupName</span></span>
<span data-ttu-id="26e06-123">Der Ressourcengruppenname des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="26e06-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="26e06-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26e06-124">-Confirm</span></span>
<span data-ttu-id="26e06-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26e06-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e06-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e06-126">-WhatIf</span></span>
<span data-ttu-id="26e06-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26e06-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e06-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26e06-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e06-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e06-129">CommonParameters</span></span>
<span data-ttu-id="26e06-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e06-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e06-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26e06-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e06-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26e06-132">INPUTS</span></span>

### <span data-ttu-id="26e06-133">System. String</span><span class="sxs-lookup"><span data-stu-id="26e06-133">System.String</span></span>

## <span data-ttu-id="26e06-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26e06-134">OUTPUTS</span></span>

### <span data-ttu-id="26e06-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26e06-135">System.Boolean</span></span>

## <span data-ttu-id="26e06-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="26e06-136">NOTES</span></span>

## <span data-ttu-id="26e06-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26e06-137">RELATED LINKS</span></span>

[<span data-ttu-id="26e06-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="26e06-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="26e06-139">Neu – AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="26e06-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)