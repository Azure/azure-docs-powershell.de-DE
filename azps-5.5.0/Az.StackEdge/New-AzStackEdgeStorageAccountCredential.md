---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155100"
---
# <span data-ttu-id="39df1-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="39df1-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="39df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39df1-102">SYNOPSIS</span></span>
<span data-ttu-id="39df1-103">Erstellt neue Anmeldeinformationen für ein Edgespeicherkonto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="39df1-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="39df1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39df1-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39df1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39df1-105">DESCRIPTION</span></span>
<span data-ttu-id="39df1-106">Das **Cmdlet "New-AzStackEdgeStorageAccountCredential"** erstellt die Anmeldeinformationen eines neuen Edgespeicherkontos für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="39df1-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="39df1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39df1-107">EXAMPLES</span></span>

### <span data-ttu-id="39df1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39df1-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="39df1-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39df1-109">PARAMETERS</span></span>

### <span data-ttu-id="39df1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39df1-110">-AsJob</span></span>
<span data-ttu-id="39df1-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="39df1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39df1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39df1-112">-DefaultProfile</span></span>
<span data-ttu-id="39df1-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39df1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39df1-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="39df1-114">-DeviceName</span></span>
<span data-ttu-id="39df1-115">Gerätename</span><span class="sxs-lookup"><span data-stu-id="39df1-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39df1-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="39df1-116">-EncryptionKey</span></span>
<span data-ttu-id="39df1-117">Verschlüsselungsschlüssel des Edgegeräts</span><span class="sxs-lookup"><span data-stu-id="39df1-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39df1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="39df1-118">-Name</span></span>
<span data-ttu-id="39df1-119">Name des zu verwendende Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="39df1-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39df1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39df1-120">-ResourceGroupName</span></span>
<span data-ttu-id="39df1-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="39df1-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39df1-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="39df1-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="39df1-123">Bereitstellen des Zugriffsschlüssels für das Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="39df1-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39df1-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="39df1-124">-StorageAccountType</span></span>
<span data-ttu-id="39df1-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="39df1-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="39df1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39df1-126">-Confirm</span></span>
<span data-ttu-id="39df1-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39df1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39df1-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="39df1-128">-WhatIf</span></span>
<span data-ttu-id="39df1-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39df1-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39df1-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39df1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39df1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39df1-131">CommonParameters</span></span>
<span data-ttu-id="39df1-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39df1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39df1-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39df1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39df1-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39df1-134">INPUTS</span></span>

### <span data-ttu-id="39df1-135">Keine</span><span class="sxs-lookup"><span data-stu-id="39df1-135">None</span></span>

## <span data-ttu-id="39df1-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39df1-136">OUTPUTS</span></span>

### <span data-ttu-id="39df1-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="39df1-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="39df1-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39df1-138">NOTES</span></span>

## <span data-ttu-id="39df1-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39df1-139">RELATED LINKS</span></span>
