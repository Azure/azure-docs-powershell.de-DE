---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178148"
---
# <span data-ttu-id="7ed63-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7ed63-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="7ed63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ed63-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed63-103">Entfernt einen Datenträger Verschlüsselungs Satz.</span><span class="sxs-lookup"><span data-stu-id="7ed63-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="7ed63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ed63-104">SYNTAX</span></span>

### <span data-ttu-id="7ed63-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ed63-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ed63-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7ed63-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ed63-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="7ed63-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ed63-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ed63-108">DESCRIPTION</span></span>
<span data-ttu-id="7ed63-109">Entfernt einen Datenträger Verschlüsselungs Satz.</span><span class="sxs-lookup"><span data-stu-id="7ed63-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="7ed63-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ed63-110">EXAMPLES</span></span>

### <span data-ttu-id="7ed63-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ed63-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="7ed63-112">Löschen des Datenträger Verschlüsselungs Satzes "ENC1" in "RG1"</span><span class="sxs-lookup"><span data-stu-id="7ed63-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="7ed63-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ed63-113">PARAMETERS</span></span>

### <span data-ttu-id="7ed63-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ed63-114">-AsJob</span></span>
<span data-ttu-id="7ed63-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7ed63-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ed63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed63-116">-DefaultProfile</span></span>
<span data-ttu-id="7ed63-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ed63-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed63-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7ed63-118">-Force</span></span>
<span data-ttu-id="7ed63-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7ed63-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ed63-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ed63-120">-InputObject</span></span>
<span data-ttu-id="7ed63-121">Das lokale Objekt des Datenträger Verschlüsselungs Satzes.</span><span class="sxs-lookup"><span data-stu-id="7ed63-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="7ed63-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7ed63-122">-Name</span></span>
<span data-ttu-id="7ed63-123">Name des Festplatten-Verschlüsselungs Satzes.</span><span class="sxs-lookup"><span data-stu-id="7ed63-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="7ed63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed63-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ed63-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7ed63-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7ed63-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7ed63-126">-ResourceId</span></span>
<span data-ttu-id="7ed63-127">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="7ed63-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="7ed63-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ed63-128">-Confirm</span></span>
<span data-ttu-id="7ed63-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ed63-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed63-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed63-130">-WhatIf</span></span>
<span data-ttu-id="7ed63-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ed63-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed63-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ed63-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed63-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed63-133">CommonParameters</span></span>
<span data-ttu-id="7ed63-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed63-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed63-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ed63-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed63-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ed63-136">INPUTS</span></span>

### <span data-ttu-id="7ed63-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7ed63-137">System.String</span></span>

### <span data-ttu-id="7ed63-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7ed63-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="7ed63-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ed63-139">OUTPUTS</span></span>

### <span data-ttu-id="7ed63-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7ed63-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7ed63-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ed63-141">NOTES</span></span>

## <span data-ttu-id="7ed63-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ed63-142">RELATED LINKS</span></span>
