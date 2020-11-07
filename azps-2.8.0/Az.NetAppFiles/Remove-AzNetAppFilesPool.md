---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: ef896185b606e107bb62208255a255655814fcbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822032"
---
# <span data-ttu-id="19b39-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="19b39-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="19b39-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19b39-102">SYNOPSIS</span></span>
<span data-ttu-id="19b39-103">Löscht einen Azure NetApp-Dateien (ANF)-Pool.</span><span class="sxs-lookup"><span data-stu-id="19b39-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="19b39-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19b39-104">SYNTAX</span></span>

### <span data-ttu-id="19b39-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="19b39-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19b39-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19b39-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19b39-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19b39-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19b39-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19b39-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19b39-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19b39-109">DESCRIPTION</span></span>
<span data-ttu-id="19b39-110">Das Cmdlet **Remove-AzNetAppFilesPool** löscht einen ANF-Pool.</span><span class="sxs-lookup"><span data-stu-id="19b39-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="19b39-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19b39-111">EXAMPLES</span></span>

### <span data-ttu-id="19b39-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19b39-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="19b39-113">Mit diesem Befehl wird der Anf-Pool "MyAnfPool" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="19b39-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="19b39-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="19b39-114">PARAMETERS</span></span>

### <span data-ttu-id="19b39-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="19b39-115">-AccountName</span></span>
<span data-ttu-id="19b39-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="19b39-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="19b39-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="19b39-117">-AccountObject</span></span>
<span data-ttu-id="19b39-118">Das Kontoobjekt, das den zu entfernenden Pool enthält</span><span class="sxs-lookup"><span data-stu-id="19b39-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="19b39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b39-119">-DefaultProfile</span></span>
<span data-ttu-id="19b39-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19b39-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19b39-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="19b39-121">-InputObject</span></span>
<span data-ttu-id="19b39-122">Das zu entfernende Pool-Objekt</span><span class="sxs-lookup"><span data-stu-id="19b39-122">The pool object to remove</span></span>

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

### <span data-ttu-id="19b39-123">-Name</span><span class="sxs-lookup"><span data-stu-id="19b39-123">-Name</span></span>
<span data-ttu-id="19b39-124">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="19b39-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="19b39-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19b39-125">-PassThru</span></span>
<span data-ttu-id="19b39-126">Zurückgeben, ob der angegebene Pool erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="19b39-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="19b39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19b39-127">-ResourceGroupName</span></span>
<span data-ttu-id="19b39-128">Die Ressourcengruppe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="19b39-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="19b39-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="19b39-129">-ResourceId</span></span>
<span data-ttu-id="19b39-130">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="19b39-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="19b39-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19b39-131">-Confirm</span></span>
<span data-ttu-id="19b39-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19b39-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19b39-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19b39-133">-WhatIf</span></span>
<span data-ttu-id="19b39-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19b39-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19b39-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19b39-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19b39-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b39-136">CommonParameters</span></span>
<span data-ttu-id="19b39-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b39-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="19b39-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b39-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b39-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19b39-139">INPUTS</span></span>

### <span data-ttu-id="19b39-140">System. String</span><span class="sxs-lookup"><span data-stu-id="19b39-140">System.String</span></span>

### <span data-ttu-id="19b39-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="19b39-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="19b39-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="19b39-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="19b39-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19b39-143">OUTPUTS</span></span>

### <span data-ttu-id="19b39-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19b39-144">System.Boolean</span></span>

## <span data-ttu-id="19b39-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="19b39-145">NOTES</span></span>

## <span data-ttu-id="19b39-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19b39-146">RELATED LINKS</span></span>
