---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010132"
---
# <span data-ttu-id="e55cb-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e55cb-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="e55cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e55cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e55cb-103">Erstellt einen Synapse-Analyse Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="e55cb-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e55cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e55cb-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e55cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e55cb-105">DESCRIPTION</span></span>
<span data-ttu-id="e55cb-106">Das Cmdlet **New-AzSynapseWorkspace** erstellt einen Azure Synapse-Analyse Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="e55cb-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e55cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e55cb-107">EXAMPLES</span></span>

### <span data-ttu-id="e55cb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e55cb-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="e55cb-109">Dieser Befehl erstellt einen Synapse-Analyse Arbeitsbereich mit dem Namen "ContosoWorkspace", der den ContosoAdlGenStorage-Datenspeicher in der Ressourcengruppe namens ContosoResourceGroup verwendet.</span><span class="sxs-lookup"><span data-stu-id="e55cb-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="e55cb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e55cb-110">PARAMETERS</span></span>

### <span data-ttu-id="e55cb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e55cb-111">-AsJob</span></span>
<span data-ttu-id="e55cb-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e55cb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e55cb-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e55cb-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="e55cb-114">Der Standardname des ADLS-Gen2-speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="e55cb-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="e55cb-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="e55cb-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="e55cb-116">Das standardmäßige ADLS-Gen2-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="e55cb-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="e55cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e55cb-117">-DefaultProfile</span></span>
<span data-ttu-id="e55cb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e55cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e55cb-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="e55cb-119">-Location</span></span>
<span data-ttu-id="e55cb-120">Azure-Bereich, in dem die Ressource erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e55cb-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="e55cb-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e55cb-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="e55cb-122">Name eines von Synapsen verwalteten virtuellen Netzwerks, das für den Azure Synapse-Arbeitsbereich dediziert ist.</span><span class="sxs-lookup"><span data-stu-id="e55cb-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

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

### <span data-ttu-id="e55cb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e55cb-123">-Name</span></span>
<span data-ttu-id="e55cb-124">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="e55cb-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e55cb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e55cb-125">-ResourceGroupName</span></span>
<span data-ttu-id="e55cb-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e55cb-126">Resource group name.</span></span>

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

### <span data-ttu-id="e55cb-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="e55cb-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="e55cb-128">SQL-Administratoranmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="e55cb-128">SQL administrator credentials.</span></span>

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

### <span data-ttu-id="e55cb-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="e55cb-129">-Tag</span></span>
<span data-ttu-id="e55cb-130">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e55cb-130">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="e55cb-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e55cb-131">-Confirm</span></span>
<span data-ttu-id="e55cb-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e55cb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e55cb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e55cb-133">-WhatIf</span></span>
<span data-ttu-id="e55cb-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e55cb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e55cb-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e55cb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e55cb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55cb-136">CommonParameters</span></span>
<span data-ttu-id="e55cb-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e55cb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55cb-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e55cb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55cb-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e55cb-139">INPUTS</span></span>

### <span data-ttu-id="e55cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e55cb-140">System.String</span></span>

### <span data-ttu-id="e55cb-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e55cb-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e55cb-142">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="e55cb-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="e55cb-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e55cb-143">OUTPUTS</span></span>

### <span data-ttu-id="e55cb-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e55cb-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e55cb-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="e55cb-145">NOTES</span></span>

## <span data-ttu-id="e55cb-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e55cb-146">RELATED LINKS</span></span>
