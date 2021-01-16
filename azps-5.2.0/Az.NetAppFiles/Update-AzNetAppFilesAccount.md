---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 525483bdb99867ae9403c95a6bc2dc83a855704a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305448"
---
# <span data-ttu-id="02cfa-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="02cfa-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="02cfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="02cfa-103">Aktualisiert ein Azure NetApp Files (ANF)-Konto entsprechend den bereitgestellten optionalen Modifizierern.</span><span class="sxs-lookup"><span data-stu-id="02cfa-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="02cfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02cfa-104">SYNTAX</span></span>

### <span data-ttu-id="02cfa-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="02cfa-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02cfa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02cfa-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02cfa-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02cfa-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02cfa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02cfa-108">DESCRIPTION</span></span>
<span data-ttu-id="02cfa-109">Das **Cmdlet "Update-AzNetAppFilesAccount"** ändert ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="02cfa-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="02cfa-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="02cfa-110">EXAMPLES</span></span>

### <span data-ttu-id="02cfa-111">Beispiel 1: Aktualisiert ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="02cfa-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="02cfa-112">Dieser Befehl führt eine Aktualisierung für das angegebene Konto durch und ändert die Markierungen an die bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="02cfa-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="02cfa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02cfa-113">PARAMETERS</span></span>

### <span data-ttu-id="02cfa-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="02cfa-114">-ActiveDirectory</span></span>
<span data-ttu-id="02cfa-115">Hashtablearray, das die aktiven Verzeichnisse darstellt</span><span class="sxs-lookup"><span data-stu-id="02cfa-115">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="02cfa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02cfa-116">-DefaultProfile</span></span>
<span data-ttu-id="02cfa-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02cfa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02cfa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02cfa-118">-InputObject</span></span>
<span data-ttu-id="02cfa-119">Das zu aktualisierende Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="02cfa-119">The account object to update</span></span>

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

### <span data-ttu-id="02cfa-120">-Location</span><span class="sxs-lookup"><span data-stu-id="02cfa-120">-Location</span></span>
<span data-ttu-id="02cfa-121">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="02cfa-121">The location of the resource</span></span>

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

### <span data-ttu-id="02cfa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="02cfa-122">-Name</span></span>
<span data-ttu-id="02cfa-123">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="02cfa-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="02cfa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02cfa-124">-ResourceGroupName</span></span>
<span data-ttu-id="02cfa-125">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="02cfa-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="02cfa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02cfa-126">-ResourceId</span></span>
<span data-ttu-id="02cfa-127">Die Ressourcen-ID des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="02cfa-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="02cfa-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="02cfa-128">-Tag</span></span>
<span data-ttu-id="02cfa-129">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="02cfa-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="02cfa-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02cfa-130">-Confirm</span></span>
<span data-ttu-id="02cfa-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02cfa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02cfa-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="02cfa-132">-WhatIf</span></span>
<span data-ttu-id="02cfa-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02cfa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02cfa-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02cfa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02cfa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02cfa-135">CommonParameters</span></span>
<span data-ttu-id="02cfa-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02cfa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02cfa-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02cfa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02cfa-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="02cfa-138">INPUTS</span></span>

### <span data-ttu-id="02cfa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="02cfa-139">System.String</span></span>

### <span data-ttu-id="02cfa-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="02cfa-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="02cfa-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="02cfa-141">OUTPUTS</span></span>

### <span data-ttu-id="02cfa-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="02cfa-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="02cfa-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="02cfa-143">NOTES</span></span>

## <span data-ttu-id="02cfa-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="02cfa-144">RELATED LINKS</span></span>
