---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458916"
---
# <span data-ttu-id="cc040-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="cc040-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="cc040-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc040-102">SYNOPSIS</span></span>
<span data-ttu-id="cc040-103">Erstellt ein neues Azure NetApp Files (ANF)-Konto.</span><span class="sxs-lookup"><span data-stu-id="cc040-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="cc040-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc040-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc040-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc040-105">DESCRIPTION</span></span>
<span data-ttu-id="cc040-106">Das **Cmdlet "New-AzNetAppFilesAccount"** erstellt ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="cc040-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="cc040-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc040-107">EXAMPLES</span></span>

### <span data-ttu-id="cc040-108">Beispiel 1: Erstellen eines ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="cc040-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="cc040-109">Mit diesem Befehl wird das neue ANF-Konto "MyAnfAccount" erstellt.</span><span class="sxs-lookup"><span data-stu-id="cc040-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="cc040-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc040-110">PARAMETERS</span></span>

### <span data-ttu-id="cc040-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="cc040-111">-ActiveDirectory</span></span>
<span data-ttu-id="cc040-112">Hashtablearray, das die aktiven Verzeichnisse darstellt</span><span class="sxs-lookup"><span data-stu-id="cc040-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="cc040-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc040-113">-DefaultProfile</span></span>
<span data-ttu-id="cc040-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc040-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc040-115">-Location</span><span class="sxs-lookup"><span data-stu-id="cc040-115">-Location</span></span>
<span data-ttu-id="cc040-116">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="cc040-116">The location of the resource</span></span>

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

### <span data-ttu-id="cc040-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cc040-117">-Name</span></span>
<span data-ttu-id="cc040-118">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="cc040-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="cc040-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc040-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc040-120">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="cc040-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="cc040-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc040-121">-Tag</span></span>
<span data-ttu-id="cc040-122">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="cc040-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="cc040-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc040-123">-Confirm</span></span>
<span data-ttu-id="cc040-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc040-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc040-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cc040-125">-WhatIf</span></span>
<span data-ttu-id="cc040-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc040-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc040-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc040-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc040-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc040-128">CommonParameters</span></span>
<span data-ttu-id="cc040-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc040-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc040-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc040-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc040-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc040-131">INPUTS</span></span>

### <span data-ttu-id="cc040-132">Keine</span><span class="sxs-lookup"><span data-stu-id="cc040-132">None</span></span>

## <span data-ttu-id="cc040-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc040-133">OUTPUTS</span></span>

### <span data-ttu-id="cc040-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="cc040-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="cc040-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cc040-135">NOTES</span></span>

## <span data-ttu-id="cc040-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cc040-136">RELATED LINKS</span></span>
