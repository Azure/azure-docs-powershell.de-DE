---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660965"
---
# <span data-ttu-id="9b05a-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9b05a-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="9b05a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b05a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b05a-103">Aktualisiert einen Azure NetApp-Dateien (ANF)-Pool mit der neuen Datengruppe.</span><span class="sxs-lookup"><span data-stu-id="9b05a-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="9b05a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b05a-104">SYNTAX</span></span>

### <span data-ttu-id="9b05a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b05a-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b05a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b05a-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b05a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b05a-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b05a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b05a-108">DESCRIPTION</span></span>
<span data-ttu-id="9b05a-109">Mit dem Cmdlet **Update-AzNetAppFilesPool** wird ein ANF-Pool geändert.</span><span class="sxs-lookup"><span data-stu-id="9b05a-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="9b05a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b05a-110">EXAMPLES</span></span>

### <span data-ttu-id="9b05a-111">Beispiel 1: Ändern eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="9b05a-111">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="9b05a-112">Mit diesem Befehl wird der Anf-Pool "MyAnfPool" so geändert, dass er die angegebene Größe und Service Level hat.</span><span class="sxs-lookup"><span data-stu-id="9b05a-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="9b05a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b05a-113">PARAMETERS</span></span>

### <span data-ttu-id="9b05a-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="9b05a-114">-AccountName</span></span>
<span data-ttu-id="9b05a-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="9b05a-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="9b05a-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="9b05a-116">-AccountObject</span></span>
<span data-ttu-id="9b05a-117">Das Kontoobjekt, das den zu aktualisierbaren Pool enthält</span><span class="sxs-lookup"><span data-stu-id="9b05a-117">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="9b05a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b05a-118">-DefaultProfile</span></span>
<span data-ttu-id="9b05a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b05a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b05a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b05a-120">-InputObject</span></span>
<span data-ttu-id="9b05a-121">Das zu aktualisierbare Pool-Objekt</span><span class="sxs-lookup"><span data-stu-id="9b05a-121">The pool object to update</span></span>

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

### <span data-ttu-id="9b05a-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="9b05a-122">-Location</span></span>
<span data-ttu-id="9b05a-123">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="9b05a-123">The location of the resource</span></span>

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

### <span data-ttu-id="9b05a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9b05a-124">-Name</span></span>
<span data-ttu-id="9b05a-125">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="9b05a-125">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9b05a-126">-Pools</span><span class="sxs-lookup"><span data-stu-id="9b05a-126">-PoolSize</span></span>
<span data-ttu-id="9b05a-127">Die Größe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="9b05a-127">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b05a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b05a-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b05a-129">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="9b05a-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9b05a-130">-Service Level</span><span class="sxs-lookup"><span data-stu-id="9b05a-130">-ServiceLevel</span></span>
<span data-ttu-id="9b05a-131">Die Dienstebene des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="9b05a-131">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b05a-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b05a-132">-Confirm</span></span>
<span data-ttu-id="9b05a-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b05a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b05a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b05a-134">-WhatIf</span></span>
<span data-ttu-id="9b05a-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b05a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b05a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b05a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b05a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b05a-137">CommonParameters</span></span>
<span data-ttu-id="9b05a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b05a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9b05a-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b05a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b05a-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b05a-140">INPUTS</span></span>

### <span data-ttu-id="9b05a-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9b05a-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="9b05a-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9b05a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="9b05a-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b05a-143">OUTPUTS</span></span>

### <span data-ttu-id="9b05a-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9b05a-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="9b05a-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b05a-145">NOTES</span></span>

## <span data-ttu-id="9b05a-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b05a-146">RELATED LINKS</span></span>
