---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 107881e8d9ac1f631b9a90dbf68ba096a59cefb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652022"
---
# <span data-ttu-id="47a15-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="47a15-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="47a15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47a15-102">SYNOPSIS</span></span>
<span data-ttu-id="47a15-103">Entfernt eine Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="47a15-103">Removes a host group.</span></span>

## <span data-ttu-id="47a15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47a15-104">SYNTAX</span></span>

### <span data-ttu-id="47a15-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="47a15-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a15-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="47a15-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a15-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="47a15-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a15-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47a15-108">DESCRIPTION</span></span>
<span data-ttu-id="47a15-109">Mit diesem Cmdlet wird eine Host Gruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="47a15-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="47a15-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47a15-110">EXAMPLES</span></span>

### <span data-ttu-id="47a15-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47a15-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="47a15-112">Dieser Befehl ruft die angegebene Hostgruppe ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="47a15-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="47a15-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="47a15-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="47a15-114">Dieser Befehl entfernt die angegebene Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="47a15-114">This command removes the given host group.</span></span>

## <span data-ttu-id="47a15-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="47a15-115">PARAMETERS</span></span>

### <span data-ttu-id="47a15-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47a15-116">-AsJob</span></span>
<span data-ttu-id="47a15-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="47a15-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47a15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a15-118">-DefaultProfile</span></span>
<span data-ttu-id="47a15-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47a15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47a15-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="47a15-120">-InputObject</span></span>
<span data-ttu-id="47a15-121">Das lokale Objekt der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="47a15-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47a15-122">-Name</span><span class="sxs-lookup"><span data-stu-id="47a15-122">-Name</span></span>
<span data-ttu-id="47a15-123">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="47a15-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47a15-124">-ResourceGroupName</span></span>
<span data-ttu-id="47a15-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="47a15-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="47a15-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="47a15-126">-ResourceId</span></span>
<span data-ttu-id="47a15-127">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="47a15-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="47a15-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47a15-128">-Confirm</span></span>
<span data-ttu-id="47a15-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47a15-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a15-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a15-130">-WhatIf</span></span>
<span data-ttu-id="47a15-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47a15-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47a15-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47a15-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a15-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a15-133">CommonParameters</span></span>
<span data-ttu-id="47a15-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a15-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a15-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47a15-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a15-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47a15-136">INPUTS</span></span>

### <span data-ttu-id="47a15-137">System. String</span><span class="sxs-lookup"><span data-stu-id="47a15-137">System.String</span></span>

### <span data-ttu-id="47a15-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="47a15-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="47a15-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47a15-139">OUTPUTS</span></span>

### <span data-ttu-id="47a15-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="47a15-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="47a15-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="47a15-141">NOTES</span></span>

## <span data-ttu-id="47a15-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47a15-142">RELATED LINKS</span></span>
