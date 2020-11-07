---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: bea1f6d9427d0ed5dca48994d8138f954ed25ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845016"
---
# <span data-ttu-id="c5fff-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c5fff-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="c5fff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5fff-102">SYNOPSIS</span></span>
<span data-ttu-id="c5fff-103">Aktualisiert einen Azure NetApp-Dateien (ANF)-Pool entsprechend den bereitgestellten optionalen Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="c5fff-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="c5fff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5fff-104">SYNTAX</span></span>

### <span data-ttu-id="c5fff-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5fff-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5fff-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5fff-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5fff-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5fff-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5fff-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5fff-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5fff-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5fff-109">DESCRIPTION</span></span>
<span data-ttu-id="c5fff-110">Mit dem Cmdlet **Update-AzNetAppFilesPool** wird ein ANF-Pool geändert.</span><span class="sxs-lookup"><span data-stu-id="c5fff-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="c5fff-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5fff-111">EXAMPLES</span></span>

### <span data-ttu-id="c5fff-112">Beispiel 1: Ändern eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c5fff-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="c5fff-113">Mit diesem Befehl wird der Anf-Pool "MyAnfPool" so geändert, dass er die angegebene Größe und Service Level hat.</span><span class="sxs-lookup"><span data-stu-id="c5fff-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="c5fff-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5fff-114">PARAMETERS</span></span>

### <span data-ttu-id="c5fff-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="c5fff-115">-AccountName</span></span>
<span data-ttu-id="c5fff-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="c5fff-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="c5fff-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="c5fff-117">-AccountObject</span></span>
<span data-ttu-id="c5fff-118">Das Kontoobjekt, das den zu aktualisierbaren Pool enthält</span><span class="sxs-lookup"><span data-stu-id="c5fff-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="c5fff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5fff-119">-DefaultProfile</span></span>
<span data-ttu-id="c5fff-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5fff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5fff-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c5fff-121">-InputObject</span></span>
<span data-ttu-id="c5fff-122">Das zu aktualisierbare Pool-Objekt</span><span class="sxs-lookup"><span data-stu-id="c5fff-122">The pool object to update</span></span>

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

### <span data-ttu-id="c5fff-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="c5fff-123">-Location</span></span>
<span data-ttu-id="c5fff-124">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="c5fff-124">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5fff-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c5fff-125">-Name</span></span>
<span data-ttu-id="c5fff-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c5fff-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c5fff-127">-Pools</span><span class="sxs-lookup"><span data-stu-id="c5fff-127">-PoolSize</span></span>
<span data-ttu-id="c5fff-128">Die Größe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c5fff-128">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5fff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5fff-129">-ResourceGroupName</span></span>
<span data-ttu-id="c5fff-130">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="c5fff-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c5fff-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c5fff-131">-ResourceId</span></span>
<span data-ttu-id="c5fff-132">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c5fff-132">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="c5fff-133">-Service Level</span><span class="sxs-lookup"><span data-stu-id="c5fff-133">-ServiceLevel</span></span>
<span data-ttu-id="c5fff-134">Die Dienstebene des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="c5fff-134">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5fff-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5fff-135">-Tag</span></span>
<span data-ttu-id="c5fff-136">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="c5fff-136">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5fff-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5fff-137">-Confirm</span></span>
<span data-ttu-id="c5fff-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5fff-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5fff-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5fff-139">-WhatIf</span></span>
<span data-ttu-id="c5fff-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5fff-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5fff-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5fff-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5fff-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5fff-142">CommonParameters</span></span>
<span data-ttu-id="c5fff-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5fff-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c5fff-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5fff-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5fff-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5fff-145">INPUTS</span></span>

### <span data-ttu-id="c5fff-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c5fff-146">System.String</span></span>

### <span data-ttu-id="c5fff-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c5fff-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="c5fff-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c5fff-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c5fff-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5fff-149">OUTPUTS</span></span>

### <span data-ttu-id="c5fff-150">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c5fff-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c5fff-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5fff-151">NOTES</span></span>

## <span data-ttu-id="c5fff-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5fff-152">RELATED LINKS</span></span>
