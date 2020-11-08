---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004113"
---
# <span data-ttu-id="454e5-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="454e5-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="454e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="454e5-102">SYNOPSIS</span></span>
<span data-ttu-id="454e5-103">Entfernt die Anmeldeinformationen eines speicherkontos für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="454e5-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="454e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="454e5-104">SYNTAX</span></span>

### <span data-ttu-id="454e5-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="454e5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="454e5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="454e5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454e5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="454e5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="454e5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="454e5-108">DESCRIPTION</span></span>
<span data-ttu-id="454e5-109">Das Cmdlet **Remove-AzStackEdgeStorageAccountCredential** entfernt die Speicherkonto Anmeldeinformationen für ein Stack-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="454e5-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="454e5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="454e5-110">EXAMPLES</span></span>

### <span data-ttu-id="454e5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="454e5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="454e5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="454e5-112">PARAMETERS</span></span>

### <span data-ttu-id="454e5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="454e5-113">-AsJob</span></span>
<span data-ttu-id="454e5-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="454e5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="454e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="454e5-115">-DefaultProfile</span></span>
<span data-ttu-id="454e5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="454e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="454e5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="454e5-117">-DeviceName</span></span>
<span data-ttu-id="454e5-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="454e5-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="454e5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="454e5-119">-InputObject</span></span>
<span data-ttu-id="454e5-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="454e5-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="454e5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="454e5-121">-Name</span></span>
<span data-ttu-id="454e5-122">Name des zu verwendenden speicherkontos</span><span class="sxs-lookup"><span data-stu-id="454e5-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="454e5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="454e5-123">-PassThru</span></span>
<span data-ttu-id="454e5-124">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="454e5-124">returns true if successful</span></span>

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

### <span data-ttu-id="454e5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="454e5-125">-ResourceGroupName</span></span>
<span data-ttu-id="454e5-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="454e5-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="454e5-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="454e5-127">-ResourceId</span></span>
<span data-ttu-id="454e5-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="454e5-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="454e5-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="454e5-129">-Confirm</span></span>
<span data-ttu-id="454e5-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="454e5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="454e5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="454e5-131">-WhatIf</span></span>
<span data-ttu-id="454e5-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="454e5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="454e5-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="454e5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="454e5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="454e5-134">CommonParameters</span></span>
<span data-ttu-id="454e5-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="454e5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="454e5-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="454e5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="454e5-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="454e5-137">INPUTS</span></span>

### <span data-ttu-id="454e5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="454e5-138">System.String</span></span>

### <span data-ttu-id="454e5-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="454e5-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="454e5-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="454e5-140">OUTPUTS</span></span>

### <span data-ttu-id="454e5-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="454e5-141">System.Boolean</span></span>

## <span data-ttu-id="454e5-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="454e5-142">NOTES</span></span>

## <span data-ttu-id="454e5-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="454e5-143">RELATED LINKS</span></span>
