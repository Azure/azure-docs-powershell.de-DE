---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: a9bb0e844101c4d21db52c2f7852e3b548d283cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944681"
---
# <span data-ttu-id="3318d-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3318d-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3318d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3318d-102">SYNOPSIS</span></span>
<span data-ttu-id="3318d-103">Erstellt neue Anmeldeinformationen für ein Edgespeicherkonto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="3318d-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="3318d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3318d-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3318d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3318d-105">DESCRIPTION</span></span>
<span data-ttu-id="3318d-106">Das **New-AzStackEdgeStorageAccountCredential-Cmdlet** erstellt ein neues Edgespeicherkontoanmeldeinformationen für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="3318d-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="3318d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3318d-107">EXAMPLES</span></span>

### <span data-ttu-id="3318d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3318d-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="3318d-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3318d-109">PARAMETERS</span></span>

### <span data-ttu-id="3318d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3318d-110">-AsJob</span></span>
<span data-ttu-id="3318d-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3318d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3318d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3318d-112">-DefaultProfile</span></span>
<span data-ttu-id="3318d-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3318d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3318d-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3318d-114">-DeviceName</span></span>
<span data-ttu-id="3318d-115">Gerätename</span><span class="sxs-lookup"><span data-stu-id="3318d-115">Device Name</span></span>

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

### <span data-ttu-id="3318d-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3318d-116">-EncryptionKey</span></span>
<span data-ttu-id="3318d-117">Verschlüsselungsschlüssel des Edgegeräts</span><span class="sxs-lookup"><span data-stu-id="3318d-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="3318d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3318d-118">-Name</span></span>
<span data-ttu-id="3318d-119">Name des zu verwendende Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3318d-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="3318d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3318d-120">-ResourceGroupName</span></span>
<span data-ttu-id="3318d-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3318d-121">Resource Group Name</span></span>

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

### <span data-ttu-id="3318d-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="3318d-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="3318d-123">Bereitstellen des Zugriffsschlüssels für speicherkonto</span><span class="sxs-lookup"><span data-stu-id="3318d-123">provide storage account access key</span></span>

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

### <span data-ttu-id="3318d-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3318d-124">-StorageAccountType</span></span>
<span data-ttu-id="3318d-125">Möglicher Speicherzugriffstyp GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="3318d-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="3318d-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3318d-126">-Confirm</span></span>
<span data-ttu-id="3318d-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3318d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3318d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3318d-128">-WhatIf</span></span>
<span data-ttu-id="3318d-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3318d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3318d-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3318d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3318d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3318d-131">CommonParameters</span></span>
<span data-ttu-id="3318d-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3318d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3318d-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3318d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3318d-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3318d-134">INPUTS</span></span>

### <span data-ttu-id="3318d-135">Keine</span><span class="sxs-lookup"><span data-stu-id="3318d-135">None</span></span>

## <span data-ttu-id="3318d-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3318d-136">OUTPUTS</span></span>

### <span data-ttu-id="3318d-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3318d-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3318d-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3318d-138">NOTES</span></span>

## <span data-ttu-id="3318d-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3318d-139">RELATED LINKS</span></span>
