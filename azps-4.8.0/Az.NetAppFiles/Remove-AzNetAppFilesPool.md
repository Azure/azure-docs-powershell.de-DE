---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010133"
---
# <span data-ttu-id="8289d-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8289d-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="8289d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8289d-102">SYNOPSIS</span></span>
<span data-ttu-id="8289d-103">Löscht einen Azure NetApp-Dateien (ANF)-Pool.</span><span class="sxs-lookup"><span data-stu-id="8289d-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="8289d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8289d-104">SYNTAX</span></span>

### <span data-ttu-id="8289d-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8289d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8289d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8289d-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8289d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8289d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8289d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8289d-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8289d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8289d-109">DESCRIPTION</span></span>
<span data-ttu-id="8289d-110">Das Cmdlet **Remove-AzNetAppFilesPool** löscht einen ANF-Pool.</span><span class="sxs-lookup"><span data-stu-id="8289d-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="8289d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8289d-111">EXAMPLES</span></span>

### <span data-ttu-id="8289d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8289d-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="8289d-113">Mit diesem Befehl wird der Anf-Pool "MyAnfPool" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8289d-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="8289d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8289d-114">PARAMETERS</span></span>

### <span data-ttu-id="8289d-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="8289d-115">-AccountName</span></span>
<span data-ttu-id="8289d-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="8289d-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8289d-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="8289d-117">-AccountObject</span></span>
<span data-ttu-id="8289d-118">Das Kontoobjekt, das den zu entfernenden Pool enthält</span><span class="sxs-lookup"><span data-stu-id="8289d-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="8289d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8289d-119">-DefaultProfile</span></span>
<span data-ttu-id="8289d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8289d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8289d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8289d-121">-InputObject</span></span>
<span data-ttu-id="8289d-122">Das zu entfernende Pool-Objekt</span><span class="sxs-lookup"><span data-stu-id="8289d-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8289d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8289d-123">-Name</span></span>
<span data-ttu-id="8289d-124">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="8289d-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8289d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8289d-125">-PassThru</span></span>
<span data-ttu-id="8289d-126">Zurückgeben, ob der angegebene Pool erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="8289d-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="8289d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8289d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8289d-128">Die Ressourcengruppe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="8289d-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="8289d-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8289d-129">-ResourceId</span></span>
<span data-ttu-id="8289d-130">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="8289d-130">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8289d-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8289d-131">-Confirm</span></span>
<span data-ttu-id="8289d-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8289d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8289d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8289d-133">-WhatIf</span></span>
<span data-ttu-id="8289d-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8289d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8289d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8289d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8289d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8289d-136">CommonParameters</span></span>
<span data-ttu-id="8289d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8289d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8289d-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8289d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8289d-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8289d-139">INPUTS</span></span>

### <span data-ttu-id="8289d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8289d-140">System.String</span></span>

### <span data-ttu-id="8289d-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8289d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8289d-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8289d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8289d-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8289d-143">OUTPUTS</span></span>

### <span data-ttu-id="8289d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8289d-144">System.Boolean</span></span>

## <span data-ttu-id="8289d-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="8289d-145">NOTES</span></span>

## <span data-ttu-id="8289d-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8289d-146">RELATED LINKS</span></span>
