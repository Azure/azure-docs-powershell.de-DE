---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171209"
---
# <span data-ttu-id="8c192-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8c192-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="8c192-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c192-102">SYNOPSIS</span></span>
<span data-ttu-id="8c192-103">Entfernt einen Datenträgerverschlüsselungssatz.</span><span class="sxs-lookup"><span data-stu-id="8c192-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="8c192-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c192-104">SYNTAX</span></span>

### <span data-ttu-id="8c192-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c192-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c192-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8c192-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c192-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8c192-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c192-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c192-108">DESCRIPTION</span></span>
<span data-ttu-id="8c192-109">Entfernt einen Datenträgerverschlüsselungssatz.</span><span class="sxs-lookup"><span data-stu-id="8c192-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="8c192-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c192-110">EXAMPLES</span></span>

### <span data-ttu-id="8c192-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c192-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="8c192-112">Löschen des Datenträgerverschlüsselungssatz 'enc1' in 'rg1'</span><span class="sxs-lookup"><span data-stu-id="8c192-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="8c192-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c192-113">PARAMETERS</span></span>

### <span data-ttu-id="8c192-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c192-114">-AsJob</span></span>
<span data-ttu-id="8c192-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8c192-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c192-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c192-116">-DefaultProfile</span></span>
<span data-ttu-id="8c192-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c192-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c192-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8c192-118">-Force</span></span>
<span data-ttu-id="8c192-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="8c192-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c192-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c192-120">-InputObject</span></span>
<span data-ttu-id="8c192-121">Das lokale Objekt des Datenträgerverschlüsselungssets.</span><span class="sxs-lookup"><span data-stu-id="8c192-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c192-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8c192-122">-Name</span></span>
<span data-ttu-id="8c192-123">Name des Datenträgerverschlüsselungssatzs.</span><span class="sxs-lookup"><span data-stu-id="8c192-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c192-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c192-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c192-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8c192-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8c192-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c192-126">-ResourceId</span></span>
<span data-ttu-id="8c192-127">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8c192-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="8c192-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c192-128">-Confirm</span></span>
<span data-ttu-id="8c192-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c192-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c192-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8c192-130">-WhatIf</span></span>
<span data-ttu-id="8c192-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c192-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c192-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c192-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c192-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c192-133">CommonParameters</span></span>
<span data-ttu-id="8c192-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c192-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c192-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c192-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c192-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c192-136">INPUTS</span></span>

### <span data-ttu-id="8c192-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8c192-137">System.String</span></span>

### <span data-ttu-id="8c192-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8c192-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="8c192-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c192-139">OUTPUTS</span></span>

### <span data-ttu-id="8c192-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8c192-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8c192-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8c192-141">NOTES</span></span>

## <span data-ttu-id="8c192-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8c192-142">RELATED LINKS</span></span>
