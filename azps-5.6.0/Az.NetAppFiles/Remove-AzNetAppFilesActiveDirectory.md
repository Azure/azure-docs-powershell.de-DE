---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ab7607dd358e7c439539e99d44b263136f07cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926795"
---
# <span data-ttu-id="92167-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="92167-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="92167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92167-102">SYNOPSIS</span></span>
<span data-ttu-id="92167-103">Löscht eine Azure NetApp Files (ANF)-Active Directory-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="92167-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="92167-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92167-104">SYNTAX</span></span>

### <span data-ttu-id="92167-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="92167-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92167-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92167-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92167-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92167-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92167-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92167-108">DESCRIPTION</span></span>
<span data-ttu-id="92167-109">Das **Cmdlet Remove-AzNetAppFilesActiveDirectory** löscht eine ANF-Active Directory-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="92167-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="92167-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92167-110">EXAMPLES</span></span>

### <span data-ttu-id="92167-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92167-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="92167-112">Mit diesem Befehl wird die neue ANF-Active Directory-Konfiguration mit dem Namen "MyADName" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="92167-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="92167-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="92167-113">PARAMETERS</span></span>

### <span data-ttu-id="92167-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="92167-114">-AccountName</span></span>
<span data-ttu-id="92167-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="92167-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92167-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="92167-116">-AccountObject</span></span>
<span data-ttu-id="92167-117">Das Konto für das Active Directory-Objekt</span><span class="sxs-lookup"><span data-stu-id="92167-117">The Account for the Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92167-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="92167-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="92167-119">Die ID des ANF-Active Directory</span><span class="sxs-lookup"><span data-stu-id="92167-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92167-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92167-120">-DefaultProfile</span></span>
<span data-ttu-id="92167-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92167-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92167-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92167-122">-InputObject</span></span>
<span data-ttu-id="92167-123">Das zu entfernende Active Directory-Objekt</span><span class="sxs-lookup"><span data-stu-id="92167-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92167-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92167-124">-PassThru</span></span>
<span data-ttu-id="92167-125">Zurückgeben, ob das angegebene Active Directory erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="92167-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="92167-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92167-126">-ResourceGroupName</span></span>
<span data-ttu-id="92167-127">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="92167-127">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92167-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92167-128">-Confirm</span></span>
<span data-ttu-id="92167-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92167-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92167-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92167-130">-WhatIf</span></span>
<span data-ttu-id="92167-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92167-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92167-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92167-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92167-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92167-133">CommonParameters</span></span>
<span data-ttu-id="92167-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92167-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92167-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92167-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92167-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92167-136">INPUTS</span></span>

### <span data-ttu-id="92167-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="92167-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="92167-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="92167-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="92167-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92167-139">OUTPUTS</span></span>

### <span data-ttu-id="92167-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="92167-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="92167-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="92167-141">NOTES</span></span>

## <span data-ttu-id="92167-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="92167-142">RELATED LINKS</span></span>
