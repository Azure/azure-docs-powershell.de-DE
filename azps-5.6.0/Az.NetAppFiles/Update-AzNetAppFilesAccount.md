---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 2a31b5af374b1bc0f6136da61aa1c3672274e913
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926688"
---
# <span data-ttu-id="d6f10-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d6f10-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d6f10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f10-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f10-103">Aktualisiert ein Azure NetApp Files (ANF)-Konto entsprechend den optionalen Modifizierern, die bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6f10-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="d6f10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6f10-104">SYNTAX</span></span>

### <span data-ttu-id="d6f10-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6f10-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f10-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6f10-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f10-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6f10-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f10-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6f10-108">DESCRIPTION</span></span>
<span data-ttu-id="d6f10-109">Das **Update-AzNetAppFilesAccount-Cmdlet** ändert ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="d6f10-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="d6f10-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6f10-110">EXAMPLES</span></span>

### <span data-ttu-id="d6f10-111">Beispiel 1: Aktualisiert ein ANF-Konto</span><span class="sxs-lookup"><span data-stu-id="d6f10-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="d6f10-112">Dieser Befehl führt eine Aktualisierung für das angegebene Konto durch, indem die Tags an die bereitgestellten Tags geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d6f10-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="d6f10-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d6f10-113">PARAMETERS</span></span>

### <span data-ttu-id="d6f10-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d6f10-114">-ActiveDirectory</span></span>
<span data-ttu-id="d6f10-115">Ein Hashtablearray, das die aktiven Verzeichnisse darstellt</span><span class="sxs-lookup"><span data-stu-id="d6f10-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f10-116">-DefaultProfile</span></span>
<span data-ttu-id="d6f10-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6f10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f10-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6f10-118">-InputObject</span></span>
<span data-ttu-id="d6f10-119">Das zu aktualisierende Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d6f10-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f10-120">-Location</span><span class="sxs-lookup"><span data-stu-id="d6f10-120">-Location</span></span>
<span data-ttu-id="d6f10-121">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="d6f10-121">The location of the resource</span></span>

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

### <span data-ttu-id="d6f10-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d6f10-122">-Name</span></span>
<span data-ttu-id="d6f10-123">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="d6f10-123">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f10-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6f10-125">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="d6f10-125">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f10-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f10-126">-ResourceId</span></span>
<span data-ttu-id="d6f10-127">Die Ressourcen-ID des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="d6f10-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="d6f10-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6f10-128">-Tag</span></span>
<span data-ttu-id="d6f10-129">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="d6f10-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d6f10-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6f10-130">-Confirm</span></span>
<span data-ttu-id="d6f10-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6f10-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f10-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f10-132">-WhatIf</span></span>
<span data-ttu-id="d6f10-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6f10-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f10-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6f10-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f10-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f10-135">CommonParameters</span></span>
<span data-ttu-id="d6f10-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f10-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f10-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6f10-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f10-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6f10-138">INPUTS</span></span>

### <span data-ttu-id="d6f10-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d6f10-139">System.String</span></span>

### <span data-ttu-id="d6f10-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d6f10-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d6f10-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6f10-141">OUTPUTS</span></span>

### <span data-ttu-id="d6f10-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d6f10-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d6f10-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d6f10-143">NOTES</span></span>

## <span data-ttu-id="d6f10-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d6f10-144">RELATED LINKS</span></span>
