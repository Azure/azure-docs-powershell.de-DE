---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143908"
---
# <span data-ttu-id="8490f-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8490f-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8490f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8490f-102">SYNOPSIS</span></span>
<span data-ttu-id="8490f-103">Legt die Anmeldeinformationen für das Speicherkonto für ein Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="8490f-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="8490f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8490f-104">SYNTAX</span></span>

### <span data-ttu-id="8490f-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8490f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8490f-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8490f-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8490f-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8490f-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8490f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8490f-108">DESCRIPTION</span></span>
<span data-ttu-id="8490f-109">Das **Cmdlet Set-AzStackEdgeStorageAccountCredential** aktualisiert die Anmeldeinformationen für das Speicherkonto, das einem Speicherkonto auf dem Stack Edge-Gerät entspricht.</span><span class="sxs-lookup"><span data-stu-id="8490f-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="8490f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8490f-110">EXAMPLES</span></span>

### <span data-ttu-id="8490f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8490f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="8490f-112">Hilft beim Drehen von Zugriffstasten für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="8490f-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="8490f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8490f-113">PARAMETERS</span></span>

### <span data-ttu-id="8490f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8490f-114">-AsJob</span></span>
<span data-ttu-id="8490f-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8490f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8490f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8490f-116">-DefaultProfile</span></span>
<span data-ttu-id="8490f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8490f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8490f-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8490f-118">-DeviceName</span></span>
<span data-ttu-id="8490f-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="8490f-119">Device Name</span></span>

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

### <span data-ttu-id="8490f-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8490f-120">-EncryptionKey</span></span>
<span data-ttu-id="8490f-121">Verschlüsselungsschlüssel des Edgegeräts</span><span class="sxs-lookup"><span data-stu-id="8490f-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="8490f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8490f-122">-InputObject</span></span>
<span data-ttu-id="8490f-123">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="8490f-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8490f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8490f-124">-Name</span></span>
<span data-ttu-id="8490f-125">Name des zu verwendende Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8490f-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8490f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8490f-126">-ResourceGroupName</span></span>
<span data-ttu-id="8490f-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8490f-127">Resource Group Name</span></span>

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

### <span data-ttu-id="8490f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8490f-128">-ResourceId</span></span>
<span data-ttu-id="8490f-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8490f-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="8490f-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="8490f-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="8490f-131">Bereitstellen des Zugriffsschlüssels für das Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="8490f-131">provide storage account access key</span></span>

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

### <span data-ttu-id="8490f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8490f-132">-Confirm</span></span>
<span data-ttu-id="8490f-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8490f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8490f-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8490f-134">-WhatIf</span></span>
<span data-ttu-id="8490f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8490f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8490f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8490f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8490f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8490f-137">CommonParameters</span></span>
<span data-ttu-id="8490f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8490f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8490f-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8490f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8490f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8490f-140">INPUTS</span></span>

### <span data-ttu-id="8490f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8490f-141">System.String</span></span>

### <span data-ttu-id="8490f-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8490f-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8490f-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8490f-143">OUTPUTS</span></span>

### <span data-ttu-id="8490f-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8490f-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8490f-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8490f-145">NOTES</span></span>

## <span data-ttu-id="8490f-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8490f-146">RELATED LINKS</span></span>
