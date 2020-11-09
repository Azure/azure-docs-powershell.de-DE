---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298654"
---
# <span data-ttu-id="3b72f-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3b72f-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3b72f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b72f-102">SYNOPSIS</span></span>
<span data-ttu-id="3b72f-103">Legt die Anmeldeinformationen für das Speicherkonto für ein Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="3b72f-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="3b72f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b72f-104">SYNTAX</span></span>

### <span data-ttu-id="3b72f-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b72f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b72f-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b72f-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b72f-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b72f-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b72f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b72f-108">DESCRIPTION</span></span>
<span data-ttu-id="3b72f-109">Das Cmdlet " **Satz-AzDataBoxEdgeStorageAccountCredential** " aktualisiert die Speicherkonto Anmeldeinformationen, die einem Speicherkonto auf dem Daten Feld Edge-Gerät entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3b72f-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="3b72f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b72f-110">EXAMPLES</span></span>

### <span data-ttu-id="3b72f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b72f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="3b72f-112">Hilfe beim Drehen von Zugriffstasten für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="3b72f-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="3b72f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b72f-113">PARAMETERS</span></span>

### <span data-ttu-id="3b72f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b72f-114">-AsJob</span></span>
<span data-ttu-id="3b72f-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3b72f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b72f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b72f-116">-DefaultProfile</span></span>
<span data-ttu-id="3b72f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b72f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b72f-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3b72f-118">-DeviceName</span></span>
<span data-ttu-id="3b72f-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="3b72f-119">Device Name</span></span>

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

### <span data-ttu-id="3b72f-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3b72f-120">-EncryptionKey</span></span>
<span data-ttu-id="3b72f-121">Verschlüsselungsschlüssel des Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="3b72f-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="3b72f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b72f-122">-InputObject</span></span>
<span data-ttu-id="3b72f-123">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="3b72f-123">Input Object</span></span>

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

### <span data-ttu-id="3b72f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3b72f-124">-Name</span></span>
<span data-ttu-id="3b72f-125">Name des zu verwendenden speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3b72f-125">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="3b72f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b72f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3b72f-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3b72f-127">Resource Group Name</span></span>

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

### <span data-ttu-id="3b72f-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3b72f-128">-ResourceId</span></span>
<span data-ttu-id="3b72f-129">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="3b72f-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="3b72f-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="3b72f-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="3b72f-131">Bereitstellen des Zugriffsschlüssels für das Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="3b72f-131">provide storage account access key</span></span>

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

### <span data-ttu-id="3b72f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b72f-132">-Confirm</span></span>
<span data-ttu-id="3b72f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b72f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b72f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b72f-134">-WhatIf</span></span>
<span data-ttu-id="3b72f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b72f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b72f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b72f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b72f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b72f-137">CommonParameters</span></span>
<span data-ttu-id="3b72f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b72f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b72f-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b72f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b72f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b72f-140">INPUTS</span></span>

### <span data-ttu-id="3b72f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3b72f-141">System.String</span></span>

### <span data-ttu-id="3b72f-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3b72f-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3b72f-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b72f-143">OUTPUTS</span></span>

### <span data-ttu-id="3b72f-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3b72f-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3b72f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b72f-145">NOTES</span></span>

## <span data-ttu-id="3b72f-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b72f-146">RELATED LINKS</span></span>
