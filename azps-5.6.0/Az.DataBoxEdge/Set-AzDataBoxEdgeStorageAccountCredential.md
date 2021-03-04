---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 214b43148020b2884013a45f26b4a03cd4ea3736
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928256"
---
# <span data-ttu-id="bd5f2-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bd5f2-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bd5f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd5f2-102">SYNOPSIS</span></span>
<span data-ttu-id="bd5f2-103">Legt die Anmeldeinformationen für das Speicherkonto für ein Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="bd5f2-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="bd5f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd5f2-104">SYNTAX</span></span>

### <span data-ttu-id="bd5f2-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd5f2-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd5f2-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd5f2-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd5f2-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd5f2-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd5f2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd5f2-108">DESCRIPTION</span></span>
<span data-ttu-id="bd5f2-109">Das **Cmdlet Set-AzDataBoxEdgeStorageAccountCredential** aktualisiert die Speicherkontoanmeldeinformationen, die einem Speicherkonto auf dem Data Box Edge-Gerät entspricht.</span><span class="sxs-lookup"><span data-stu-id="bd5f2-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="bd5f2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd5f2-110">EXAMPLES</span></span>

### <span data-ttu-id="bd5f2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd5f2-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="bd5f2-112">Hilft beim Drehen von Zugriffstasten für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="bd5f2-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="bd5f2-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bd5f2-113">PARAMETERS</span></span>

### <span data-ttu-id="bd5f2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd5f2-114">-AsJob</span></span>
<span data-ttu-id="bd5f2-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bd5f2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd5f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd5f2-116">-DefaultProfile</span></span>
<span data-ttu-id="bd5f2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd5f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd5f2-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bd5f2-118">-DeviceName</span></span>
<span data-ttu-id="bd5f2-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="bd5f2-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5f2-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bd5f2-120">-EncryptionKey</span></span>
<span data-ttu-id="bd5f2-121">Verschlüsselungsschlüssel des Edgegeräts</span><span class="sxs-lookup"><span data-stu-id="bd5f2-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="bd5f2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd5f2-122">-InputObject</span></span>
<span data-ttu-id="bd5f2-123">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="bd5f2-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5f2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bd5f2-124">-Name</span></span>
<span data-ttu-id="bd5f2-125">Name des zu verwendende Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="bd5f2-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd5f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd5f2-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="bd5f2-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5f2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd5f2-128">-ResourceId</span></span>
<span data-ttu-id="bd5f2-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd5f2-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5f2-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="bd5f2-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="bd5f2-131">Bereitstellen des Zugriffsschlüssels für speicherkonto</span><span class="sxs-lookup"><span data-stu-id="bd5f2-131">provide storage account access key</span></span>

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

### <span data-ttu-id="bd5f2-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd5f2-132">-Confirm</span></span>
<span data-ttu-id="bd5f2-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd5f2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd5f2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd5f2-134">-WhatIf</span></span>
<span data-ttu-id="bd5f2-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd5f2-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd5f2-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd5f2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd5f2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd5f2-137">CommonParameters</span></span>
<span data-ttu-id="bd5f2-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd5f2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd5f2-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd5f2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd5f2-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd5f2-140">INPUTS</span></span>

### <span data-ttu-id="bd5f2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bd5f2-141">System.String</span></span>

### <span data-ttu-id="bd5f2-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bd5f2-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bd5f2-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd5f2-143">OUTPUTS</span></span>

### <span data-ttu-id="bd5f2-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bd5f2-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bd5f2-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bd5f2-145">NOTES</span></span>

## <span data-ttu-id="bd5f2-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bd5f2-146">RELATED LINKS</span></span>
