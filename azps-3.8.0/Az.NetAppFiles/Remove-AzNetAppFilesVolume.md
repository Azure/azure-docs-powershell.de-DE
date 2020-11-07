---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: cbbf68dfa3d71da40e22dc608c4933b65f953c7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845047"
---
# <span data-ttu-id="928d8-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="928d8-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="928d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="928d8-102">SYNOPSIS</span></span>
<span data-ttu-id="928d8-103">Löscht ein Azure NetApp-Dateien (ANF)-Volume.</span><span class="sxs-lookup"><span data-stu-id="928d8-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="928d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="928d8-104">SYNTAX</span></span>

### <span data-ttu-id="928d8-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="928d8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="928d8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="928d8-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="928d8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="928d8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="928d8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="928d8-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="928d8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="928d8-109">DESCRIPTION</span></span>
<span data-ttu-id="928d8-110">Das Cmdlet **Remove-AzNetAppFilesVolume** löscht ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="928d8-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="928d8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="928d8-111">EXAMPLES</span></span>

### <span data-ttu-id="928d8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="928d8-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="928d8-113">Mit diesem Befehl wird die Anf-Lautstärke "MyAnfVolume" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="928d8-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="928d8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="928d8-114">PARAMETERS</span></span>

### <span data-ttu-id="928d8-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="928d8-115">-AccountName</span></span>
<span data-ttu-id="928d8-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="928d8-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928d8-117">-DefaultProfile</span></span>
<span data-ttu-id="928d8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="928d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="928d8-119">-InputObject</span></span>
<span data-ttu-id="928d8-120">Das zu entfernende Volume-Objekt</span><span class="sxs-lookup"><span data-stu-id="928d8-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="928d8-121">-Name</span></span>
<span data-ttu-id="928d8-122">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="928d8-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="928d8-123">-PassThru</span></span>
<span data-ttu-id="928d8-124">Zurückgeben, ob das angegebene Volume erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="928d8-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-125">-Poolname</span><span class="sxs-lookup"><span data-stu-id="928d8-125">-PoolName</span></span>
<span data-ttu-id="928d8-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="928d8-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="928d8-127">-PoolObject</span></span>
<span data-ttu-id="928d8-128">Das Pool-Objekt, das das zu entfernende Volume enthält</span><span class="sxs-lookup"><span data-stu-id="928d8-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="928d8-129">-ResourceGroupName</span></span>
<span data-ttu-id="928d8-130">Die Ressourcengruppe des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="928d8-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="928d8-131">-ResourceId</span></span>
<span data-ttu-id="928d8-132">Die Ressourcen-ID des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="928d8-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="928d8-133">-Confirm</span></span>
<span data-ttu-id="928d8-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="928d8-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="928d8-135">-WhatIf</span></span>
<span data-ttu-id="928d8-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="928d8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="928d8-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="928d8-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928d8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928d8-138">CommonParameters</span></span>
<span data-ttu-id="928d8-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="928d8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="928d8-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928d8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928d8-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="928d8-141">INPUTS</span></span>

### <span data-ttu-id="928d8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="928d8-142">System.String</span></span>

### <span data-ttu-id="928d8-143">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="928d8-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="928d8-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="928d8-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="928d8-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="928d8-145">OUTPUTS</span></span>

### <span data-ttu-id="928d8-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="928d8-146">System.Boolean</span></span>

## <span data-ttu-id="928d8-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="928d8-147">NOTES</span></span>

## <span data-ttu-id="928d8-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="928d8-148">RELATED LINKS</span></span>
