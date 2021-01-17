---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364886"
---
# <span data-ttu-id="110db-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="110db-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="110db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="110db-102">SYNOPSIS</span></span>
<span data-ttu-id="110db-103">Aktualisiert ein Azure NetApp Files (ANF)-Konto mit dem neuen Datenset.</span><span class="sxs-lookup"><span data-stu-id="110db-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="110db-104">Hilfreich beim Löschen von zugeordneten aktiven Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="110db-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="110db-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="110db-105">SYNTAX</span></span>

### <span data-ttu-id="110db-106">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="110db-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="110db-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="110db-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="110db-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="110db-108">DESCRIPTION</span></span>
<span data-ttu-id="110db-109">Das **Cmdlet Set-AzNetAppFilesAccount** ändert ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="110db-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="110db-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="110db-110">EXAMPLES</span></span>

### <span data-ttu-id="110db-111">Beispiel 1: Ändern eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="110db-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="110db-112">Dieser Befehl führt eine Aktualisierung für das angegebene Konto aus.</span><span class="sxs-lookup"><span data-stu-id="110db-112">This command performs an update on the given account.</span></span> <span data-ttu-id="110db-113">Das Fehlen des aktiven Verzeichnisses bedeutet, dass es aus dem Konto entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="110db-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="110db-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="110db-114">PARAMETERS</span></span>

### <span data-ttu-id="110db-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="110db-115">-ActiveDirectory</span></span>
<span data-ttu-id="110db-116">Hashtablearray, das die aktiven Verzeichnisse darstellt</span><span class="sxs-lookup"><span data-stu-id="110db-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="110db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110db-117">-DefaultProfile</span></span>
<span data-ttu-id="110db-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="110db-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="110db-119">-Location</span><span class="sxs-lookup"><span data-stu-id="110db-119">-Location</span></span>
<span data-ttu-id="110db-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="110db-120">The location of the resource</span></span>

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

### <span data-ttu-id="110db-121">-Name</span><span class="sxs-lookup"><span data-stu-id="110db-121">-Name</span></span>
<span data-ttu-id="110db-122">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="110db-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="110db-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="110db-123">-ResourceGroupName</span></span>
<span data-ttu-id="110db-124">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="110db-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="110db-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="110db-125">-Tag</span></span>
<span data-ttu-id="110db-126">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="110db-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="110db-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="110db-127">-Confirm</span></span>
<span data-ttu-id="110db-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="110db-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="110db-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="110db-129">-WhatIf</span></span>
<span data-ttu-id="110db-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="110db-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="110db-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="110db-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="110db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110db-132">CommonParameters</span></span>
<span data-ttu-id="110db-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="110db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110db-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="110db-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110db-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="110db-135">INPUTS</span></span>

### <span data-ttu-id="110db-136">Keine</span><span class="sxs-lookup"><span data-stu-id="110db-136">None</span></span>

## <span data-ttu-id="110db-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="110db-137">OUTPUTS</span></span>

### <span data-ttu-id="110db-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="110db-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="110db-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="110db-139">NOTES</span></span>

## <span data-ttu-id="110db-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="110db-140">RELATED LINKS</span></span>
