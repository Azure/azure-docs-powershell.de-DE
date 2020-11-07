---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847644"
---
# <span data-ttu-id="97794-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="97794-101">Remove-AzHost</span></span>

## <span data-ttu-id="97794-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97794-102">SYNOPSIS</span></span>
<span data-ttu-id="97794-103">Entfernt einen Host.</span><span class="sxs-lookup"><span data-stu-id="97794-103">Removes a host.</span></span>

## <span data-ttu-id="97794-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97794-104">SYNTAX</span></span>

### <span data-ttu-id="97794-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="97794-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97794-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="97794-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97794-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="97794-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97794-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97794-108">DESCRIPTION</span></span>
<span data-ttu-id="97794-109">Mit diesem Cmdlet wird ein Host gelöscht</span><span class="sxs-lookup"><span data-stu-id="97794-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="97794-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97794-110">EXAMPLES</span></span>

### <span data-ttu-id="97794-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97794-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="97794-112">Dieser Befehl ruft den angegebenen Host ab und entfernt ihn.</span><span class="sxs-lookup"><span data-stu-id="97794-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="97794-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="97794-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="97794-114">Mit diesem Befehl wird der angegebene Host entfernt.</span><span class="sxs-lookup"><span data-stu-id="97794-114">This command removes the given host.</span></span>

## <span data-ttu-id="97794-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="97794-115">PARAMETERS</span></span>

### <span data-ttu-id="97794-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97794-116">-AsJob</span></span>
<span data-ttu-id="97794-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="97794-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97794-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97794-118">-DefaultProfile</span></span>
<span data-ttu-id="97794-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97794-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97794-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="97794-120">-HostGroupName</span></span>
<span data-ttu-id="97794-121">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="97794-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97794-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="97794-122">-InputObject</span></span>
<span data-ttu-id="97794-123">Das lokale Objekt des Hosts.</span><span class="sxs-lookup"><span data-stu-id="97794-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97794-124">-Name</span><span class="sxs-lookup"><span data-stu-id="97794-124">-Name</span></span>
<span data-ttu-id="97794-125">Der Name des Hosts.</span><span class="sxs-lookup"><span data-stu-id="97794-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97794-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97794-126">-ResourceGroupName</span></span>
<span data-ttu-id="97794-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97794-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97794-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="97794-128">-ResourceId</span></span>
<span data-ttu-id="97794-129">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="97794-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97794-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="97794-130">-Confirm</span></span>
<span data-ttu-id="97794-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="97794-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97794-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97794-132">-WhatIf</span></span>
<span data-ttu-id="97794-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97794-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97794-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97794-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97794-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97794-135">CommonParameters</span></span>
<span data-ttu-id="97794-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97794-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97794-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97794-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97794-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97794-138">INPUTS</span></span>

### <span data-ttu-id="97794-139">System. String</span><span class="sxs-lookup"><span data-stu-id="97794-139">System.String</span></span>

### <span data-ttu-id="97794-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="97794-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="97794-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97794-141">OUTPUTS</span></span>

### <span data-ttu-id="97794-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="97794-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="97794-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="97794-143">NOTES</span></span>

## <span data-ttu-id="97794-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97794-144">RELATED LINKS</span></span>
