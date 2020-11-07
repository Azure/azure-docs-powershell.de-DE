---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 717c1cac6def6fb51f1ab8b598f15a05a7d62db4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845032"
---
# <span data-ttu-id="03376-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="03376-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="03376-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03376-102">SYNOPSIS</span></span>
<span data-ttu-id="03376-103">Löscht einen Azure NetApp-Dateien (ANF)-Pool.</span><span class="sxs-lookup"><span data-stu-id="03376-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="03376-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03376-104">SYNTAX</span></span>

### <span data-ttu-id="03376-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="03376-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03376-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03376-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03376-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03376-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03376-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03376-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03376-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03376-109">DESCRIPTION</span></span>
<span data-ttu-id="03376-110">Das Cmdlet **Remove-AzNetAppFilesPool** löscht einen ANF-Pool.</span><span class="sxs-lookup"><span data-stu-id="03376-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="03376-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03376-111">EXAMPLES</span></span>

### <span data-ttu-id="03376-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03376-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="03376-113">Mit diesem Befehl wird der Anf-Pool "MyAnfPool" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="03376-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="03376-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="03376-114">PARAMETERS</span></span>

### <span data-ttu-id="03376-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="03376-115">-AccountName</span></span>
<span data-ttu-id="03376-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="03376-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="03376-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="03376-117">-AccountObject</span></span>
<span data-ttu-id="03376-118">Das Kontoobjekt, das den zu entfernenden Pool enthält</span><span class="sxs-lookup"><span data-stu-id="03376-118">The account object containing the pool to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03376-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03376-119">-DefaultProfile</span></span>
<span data-ttu-id="03376-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03376-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03376-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03376-121">-InputObject</span></span>
<span data-ttu-id="03376-122">Das zu entfernende Pool-Objekt</span><span class="sxs-lookup"><span data-stu-id="03376-122">The pool object to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03376-123">-Name</span><span class="sxs-lookup"><span data-stu-id="03376-123">-Name</span></span>
<span data-ttu-id="03376-124">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="03376-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03376-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03376-125">-PassThru</span></span>
<span data-ttu-id="03376-126">Zurückgeben, ob der angegebene Pool erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="03376-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="03376-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03376-127">-ResourceGroupName</span></span>
<span data-ttu-id="03376-128">Die Ressourcengruppe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="03376-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="03376-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="03376-129">-ResourceId</span></span>
<span data-ttu-id="03376-130">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="03376-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="03376-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03376-131">-Confirm</span></span>
<span data-ttu-id="03376-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03376-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03376-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03376-133">-WhatIf</span></span>
<span data-ttu-id="03376-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03376-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03376-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03376-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03376-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03376-136">CommonParameters</span></span>
<span data-ttu-id="03376-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03376-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="03376-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03376-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03376-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03376-139">INPUTS</span></span>

### <span data-ttu-id="03376-140">System. String</span><span class="sxs-lookup"><span data-stu-id="03376-140">System.String</span></span>

### <span data-ttu-id="03376-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="03376-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="03376-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="03376-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="03376-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03376-143">OUTPUTS</span></span>

### <span data-ttu-id="03376-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03376-144">System.Boolean</span></span>

## <span data-ttu-id="03376-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="03376-145">NOTES</span></span>

## <span data-ttu-id="03376-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03376-146">RELATED LINKS</span></span>
