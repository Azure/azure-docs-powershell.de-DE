---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: 28f1486375e0efc1f9b1b3f9a18f12050dafd799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944387"
---
# <span data-ttu-id="4711e-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4711e-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="4711e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4711e-102">SYNOPSIS</span></span>
<span data-ttu-id="4711e-103">Erstellt einen Synapse Analytics-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4711e-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="4711e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4711e-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4711e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4711e-105">DESCRIPTION</span></span>
<span data-ttu-id="4711e-106">Das **Cmdlet New-AzSynapseWorkspace** erstellt einen Azure Synapse Analytics-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4711e-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="4711e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4711e-107">EXAMPLES</span></span>

### <span data-ttu-id="4711e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4711e-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="4711e-109">Mit diesem Befehl wird ein Synapse Analytics-Arbeitsbereich namens ContosoWorkspace erstellt, der den ContosoAdlGenStorage-Datenspeicher in der Ressourcengruppe ContosoResourceGroup verwendet.</span><span class="sxs-lookup"><span data-stu-id="4711e-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="4711e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4711e-110">PARAMETERS</span></span>

### <span data-ttu-id="4711e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4711e-111">-AsJob</span></span>
<span data-ttu-id="4711e-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4711e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4711e-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4711e-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="4711e-114">Der Standardmäßige ADLS Gen2-Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="4711e-114">The default ADLS Gen2 storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4711e-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="4711e-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="4711e-116">Das standardmäßige ADLS Gen2-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="4711e-116">The default ADLS Gen2 file system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4711e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4711e-117">-DefaultProfile</span></span>
<span data-ttu-id="4711e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4711e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4711e-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4711e-119">-Location</span></span>
<span data-ttu-id="4711e-120">Azure-Region, in der die Ressource erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4711e-120">Azure region where the resource should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4711e-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4711e-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="4711e-122">Name eines von Synapse verwalteten virtuellen Netzwerks, das für den Azure Synapse-Arbeitsbereich gewidmet ist.</span><span class="sxs-lookup"><span data-stu-id="4711e-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4711e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4711e-123">-Name</span></span>
<span data-ttu-id="4711e-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="4711e-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4711e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4711e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4711e-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4711e-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4711e-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="4711e-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="4711e-128">SQL Administratoranmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="4711e-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4711e-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="4711e-129">-Tag</span></span>
<span data-ttu-id="4711e-130">Eine Zeichenfolge, ein Zeichenfolgenwörterbuch mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4711e-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4711e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4711e-131">-Confirm</span></span>
<span data-ttu-id="4711e-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4711e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4711e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4711e-133">-WhatIf</span></span>
<span data-ttu-id="4711e-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4711e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4711e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4711e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4711e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4711e-136">CommonParameters</span></span>
<span data-ttu-id="4711e-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4711e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4711e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4711e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4711e-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4711e-139">INPUTS</span></span>

### <span data-ttu-id="4711e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4711e-140">System.String</span></span>

### <span data-ttu-id="4711e-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4711e-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4711e-142">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="4711e-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="4711e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4711e-143">OUTPUTS</span></span>

### <span data-ttu-id="4711e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4711e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4711e-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4711e-145">NOTES</span></span>

## <span data-ttu-id="4711e-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4711e-146">RELATED LINKS</span></span>
