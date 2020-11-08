---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e63812f1972effd7956911861e5c6e07436fd4c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179591"
---
# <span data-ttu-id="e9427-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e9427-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="e9427-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9427-102">SYNOPSIS</span></span>
<span data-ttu-id="e9427-103">Aktualisiert einen Azure NetApp-Dateien (ANF)-Pool entsprechend den bereitgestellten optionalen Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="e9427-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="e9427-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9427-104">SYNTAX</span></span>

### <span data-ttu-id="e9427-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9427-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9427-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9427-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9427-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9427-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9427-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9427-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9427-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9427-109">DESCRIPTION</span></span>
<span data-ttu-id="e9427-110">Mit dem Cmdlet **Update-AzNetAppFilesPool** wird ein ANF-Pool geändert.</span><span class="sxs-lookup"><span data-stu-id="e9427-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="e9427-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9427-111">EXAMPLES</span></span>

### <span data-ttu-id="e9427-112">Beispiel 1: Ändern eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="e9427-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="e9427-113">Mit diesem Befehl wird der Anf-Pool "MyAnfPool" so geändert, dass er die angegebene Größe und Service Level hat.</span><span class="sxs-lookup"><span data-stu-id="e9427-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="e9427-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9427-114">PARAMETERS</span></span>

### <span data-ttu-id="e9427-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="e9427-115">-AccountName</span></span>
<span data-ttu-id="e9427-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="e9427-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="e9427-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="e9427-117">-AccountObject</span></span>
<span data-ttu-id="e9427-118">Das Kontoobjekt, das den zu aktualisierbaren Pool enthält</span><span class="sxs-lookup"><span data-stu-id="e9427-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="e9427-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9427-119">-DefaultProfile</span></span>
<span data-ttu-id="e9427-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9427-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9427-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e9427-121">-InputObject</span></span>
<span data-ttu-id="e9427-122">Das zu aktualisierbare Pool-Objekt</span><span class="sxs-lookup"><span data-stu-id="e9427-122">The pool object to update</span></span>

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

### <span data-ttu-id="e9427-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="e9427-123">-Location</span></span>
<span data-ttu-id="e9427-124">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="e9427-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9427-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e9427-125">-Name</span></span>
<span data-ttu-id="e9427-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="e9427-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="e9427-127">-Pools</span><span class="sxs-lookup"><span data-stu-id="e9427-127">-PoolSize</span></span>
<span data-ttu-id="e9427-128">Die Größe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="e9427-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9427-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9427-129">-ResourceGroupName</span></span>
<span data-ttu-id="e9427-130">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="e9427-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e9427-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e9427-131">-ResourceId</span></span>
<span data-ttu-id="e9427-132">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="e9427-132">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="e9427-133">-Service Level</span><span class="sxs-lookup"><span data-stu-id="e9427-133">-ServiceLevel</span></span>
<span data-ttu-id="e9427-134">Die Dienstebene des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="e9427-134">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9427-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9427-135">-Tag</span></span>
<span data-ttu-id="e9427-136">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="e9427-136">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9427-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9427-137">-Confirm</span></span>
<span data-ttu-id="e9427-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9427-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9427-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9427-139">-WhatIf</span></span>
<span data-ttu-id="e9427-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9427-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9427-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9427-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9427-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9427-142">CommonParameters</span></span>
<span data-ttu-id="e9427-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9427-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9427-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9427-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9427-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9427-145">INPUTS</span></span>

### <span data-ttu-id="e9427-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e9427-146">System.String</span></span>

### <span data-ttu-id="e9427-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e9427-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="e9427-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e9427-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="e9427-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9427-149">OUTPUTS</span></span>

### <span data-ttu-id="e9427-150">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e9427-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="e9427-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9427-151">NOTES</span></span>

## <span data-ttu-id="e9427-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9427-152">RELATED LINKS</span></span>
