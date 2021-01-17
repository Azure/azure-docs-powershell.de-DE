---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360042"
---
# <span data-ttu-id="334b5-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="334b5-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="334b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="334b5-102">SYNOPSIS</span></span>
<span data-ttu-id="334b5-103">Ruft Details einer Azure NetApp Files (ANF)-Momentaufnahmerichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="334b5-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="334b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="334b5-104">SYNTAX</span></span>

### <span data-ttu-id="334b5-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="334b5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334b5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="334b5-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334b5-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="334b5-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="334b5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="334b5-108">DESCRIPTION</span></span>
<span data-ttu-id="334b5-109">Das **Cmdlet "Get-AzNetAppFilesSnapshotPolicy"** ruft Details zu einer ANF-Momentaufnahmerichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="334b5-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="334b5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="334b5-110">EXAMPLES</span></span>

### <span data-ttu-id="334b5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="334b5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="334b5-112">Dieser Befehl ruft die Sicherungsrichtlinie mit dem Namen "MyBackupPolicy" für das Konto "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="334b5-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="334b5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="334b5-113">PARAMETERS</span></span>

### <span data-ttu-id="334b5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="334b5-114">-AccountName</span></span>
<span data-ttu-id="334b5-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="334b5-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="334b5-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="334b5-116">-AccountObject</span></span>
<span data-ttu-id="334b5-117">Das Konto für das neue Snapshotrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="334b5-117">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="334b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="334b5-118">-DefaultProfile</span></span>
<span data-ttu-id="334b5-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="334b5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="334b5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="334b5-120">-Name</span></span>
<span data-ttu-id="334b5-121">Der Name der ANF-Momentaufnahmerichtlinie</span><span class="sxs-lookup"><span data-stu-id="334b5-121">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="334b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="334b5-122">-ResourceGroupName</span></span>
<span data-ttu-id="334b5-123">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="334b5-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="334b5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="334b5-124">-ResourceId</span></span>
<span data-ttu-id="334b5-125">Die Ressourcen-ID der ANF-Momentaufnahmerichtlinie</span><span class="sxs-lookup"><span data-stu-id="334b5-125">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="334b5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="334b5-126">-Confirm</span></span>
<span data-ttu-id="334b5-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="334b5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="334b5-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="334b5-128">-WhatIf</span></span>
<span data-ttu-id="334b5-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="334b5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="334b5-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="334b5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="334b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334b5-131">CommonParameters</span></span>
<span data-ttu-id="334b5-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="334b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334b5-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="334b5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334b5-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="334b5-134">INPUTS</span></span>

### <span data-ttu-id="334b5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="334b5-135">System.String</span></span>

### <span data-ttu-id="334b5-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="334b5-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="334b5-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="334b5-137">OUTPUTS</span></span>

### <span data-ttu-id="334b5-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="334b5-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="334b5-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="334b5-139">NOTES</span></span>

## <span data-ttu-id="334b5-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="334b5-140">RELATED LINKS</span></span>
