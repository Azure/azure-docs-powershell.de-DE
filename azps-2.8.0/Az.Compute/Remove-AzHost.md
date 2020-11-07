---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: c2b2b1984a61c70d82ed29e434ab5959acaee632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652023"
---
# <span data-ttu-id="d601d-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="d601d-101">Remove-AzHost</span></span>

## <span data-ttu-id="d601d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d601d-102">SYNOPSIS</span></span>
<span data-ttu-id="d601d-103">Entfernt einen Host.</span><span class="sxs-lookup"><span data-stu-id="d601d-103">Removes a host.</span></span>

## <span data-ttu-id="d601d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d601d-104">SYNTAX</span></span>

### <span data-ttu-id="d601d-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="d601d-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d601d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d601d-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d601d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d601d-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d601d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d601d-108">DESCRIPTION</span></span>
<span data-ttu-id="d601d-109">Mit diesem Cmdlet wird ein Host gelöscht</span><span class="sxs-lookup"><span data-stu-id="d601d-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="d601d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d601d-110">EXAMPLES</span></span>

### <span data-ttu-id="d601d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d601d-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="d601d-112">Dieser Befehl ruft den angegebenen Host ab und entfernt ihn.</span><span class="sxs-lookup"><span data-stu-id="d601d-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="d601d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d601d-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="d601d-114">Mit diesem Befehl wird der angegebene Host entfernt.</span><span class="sxs-lookup"><span data-stu-id="d601d-114">This command removes the given host.</span></span>

## <span data-ttu-id="d601d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d601d-115">PARAMETERS</span></span>

### <span data-ttu-id="d601d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d601d-116">-AsJob</span></span>
<span data-ttu-id="d601d-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d601d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d601d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d601d-118">-DefaultProfile</span></span>
<span data-ttu-id="d601d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d601d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d601d-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="d601d-120">-HostGroupName</span></span>
<span data-ttu-id="d601d-121">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="d601d-121">The name of the host group.</span></span>

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

### <span data-ttu-id="d601d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d601d-122">-InputObject</span></span>
<span data-ttu-id="d601d-123">Das lokale Objekt des Hosts.</span><span class="sxs-lookup"><span data-stu-id="d601d-123">The local object of the host.</span></span>

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

### <span data-ttu-id="d601d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d601d-124">-Name</span></span>
<span data-ttu-id="d601d-125">Der Name des Hosts.</span><span class="sxs-lookup"><span data-stu-id="d601d-125">The name of the host.</span></span>

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

### <span data-ttu-id="d601d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d601d-126">-ResourceGroupName</span></span>
<span data-ttu-id="d601d-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d601d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d601d-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d601d-128">-ResourceId</span></span>
<span data-ttu-id="d601d-129">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d601d-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="d601d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d601d-130">-Confirm</span></span>
<span data-ttu-id="d601d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d601d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d601d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d601d-132">-WhatIf</span></span>
<span data-ttu-id="d601d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d601d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d601d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d601d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d601d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d601d-135">CommonParameters</span></span>
<span data-ttu-id="d601d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d601d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d601d-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d601d-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d601d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d601d-138">INPUTS</span></span>

### <span data-ttu-id="d601d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d601d-139">System.String</span></span>

### <span data-ttu-id="d601d-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="d601d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="d601d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d601d-141">OUTPUTS</span></span>

### <span data-ttu-id="d601d-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d601d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d601d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="d601d-143">NOTES</span></span>

## <span data-ttu-id="d601d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d601d-144">RELATED LINKS</span></span>
