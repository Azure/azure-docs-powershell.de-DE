---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 3e93792a8698999599f67be84c3fe01e9c2ae508
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926904"
---
# <span data-ttu-id="66491-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="66491-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="66491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66491-102">SYNOPSIS</span></span>
<span data-ttu-id="66491-103">Ruft Details einer Azure NetApp Files (ANF)-Snapshotrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="66491-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="66491-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66491-104">SYNTAX</span></span>

### <span data-ttu-id="66491-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="66491-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66491-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66491-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66491-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66491-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66491-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66491-108">DESCRIPTION</span></span>
<span data-ttu-id="66491-109">Das **Cmdlet Get-AzNetAppFilesSnapshotPolicy** ruft Details einer ANF-Snapshotrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="66491-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="66491-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66491-110">EXAMPLES</span></span>

### <span data-ttu-id="66491-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66491-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="66491-112">Dieser Befehl ruft die Sicherungsrichtlinie mit dem Namen "MyBackupPolicy" für das Konto "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="66491-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="66491-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66491-113">PARAMETERS</span></span>

### <span data-ttu-id="66491-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66491-114">-AccountName</span></span>
<span data-ttu-id="66491-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="66491-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="66491-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="66491-116">-AccountObject</span></span>
<span data-ttu-id="66491-117">Das Konto für das neue Snapshotrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="66491-117">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="66491-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66491-118">-DefaultProfile</span></span>
<span data-ttu-id="66491-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66491-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66491-120">-Name</span><span class="sxs-lookup"><span data-stu-id="66491-120">-Name</span></span>
<span data-ttu-id="66491-121">Der Name der ANF-Momentaufnahmerichtlinie</span><span class="sxs-lookup"><span data-stu-id="66491-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66491-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66491-122">-ResourceGroupName</span></span>
<span data-ttu-id="66491-123">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="66491-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="66491-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66491-124">-ResourceId</span></span>
<span data-ttu-id="66491-125">Die Ressourcen-ID der ANF-Momentaufnahmerichtlinie</span><span class="sxs-lookup"><span data-stu-id="66491-125">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="66491-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66491-126">-Confirm</span></span>
<span data-ttu-id="66491-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66491-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66491-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66491-128">-WhatIf</span></span>
<span data-ttu-id="66491-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66491-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66491-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66491-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66491-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66491-131">CommonParameters</span></span>
<span data-ttu-id="66491-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66491-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66491-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66491-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66491-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66491-134">INPUTS</span></span>

### <span data-ttu-id="66491-135">System.String</span><span class="sxs-lookup"><span data-stu-id="66491-135">System.String</span></span>

### <span data-ttu-id="66491-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="66491-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="66491-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66491-137">OUTPUTS</span></span>

### <span data-ttu-id="66491-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="66491-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="66491-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66491-139">NOTES</span></span>

## <span data-ttu-id="66491-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66491-140">RELATED LINKS</span></span>
