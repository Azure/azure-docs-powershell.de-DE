---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302969"
---
# <span data-ttu-id="29254-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="29254-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="29254-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29254-102">SYNOPSIS</span></span>
<span data-ttu-id="29254-103">Erstellt neue Anmeldeinformationen für ein Edge-Speicherkonto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="29254-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="29254-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29254-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29254-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29254-105">DESCRIPTION</span></span>
<span data-ttu-id="29254-106">Das Cmdlet **New-AzStackEdgeStorageAccountCredential** erstellt eine neue Anmeldeinformationen für ein Edge-Speicherkonto für ein Stack-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="29254-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="29254-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29254-107">EXAMPLES</span></span>

### <span data-ttu-id="29254-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29254-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="29254-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="29254-109">PARAMETERS</span></span>

### <span data-ttu-id="29254-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29254-110">-AsJob</span></span>
<span data-ttu-id="29254-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29254-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29254-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29254-112">-DefaultProfile</span></span>
<span data-ttu-id="29254-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29254-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29254-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="29254-114">-DeviceName</span></span>
<span data-ttu-id="29254-115">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="29254-115">Device Name</span></span>

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

### <span data-ttu-id="29254-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="29254-116">-EncryptionKey</span></span>
<span data-ttu-id="29254-117">Verschlüsselungsschlüssel des Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="29254-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="29254-118">-Name</span><span class="sxs-lookup"><span data-stu-id="29254-118">-Name</span></span>
<span data-ttu-id="29254-119">Name des zu verwendenden speicherkontos</span><span class="sxs-lookup"><span data-stu-id="29254-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="29254-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29254-120">-ResourceGroupName</span></span>
<span data-ttu-id="29254-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="29254-121">Resource Group Name</span></span>

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

### <span data-ttu-id="29254-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="29254-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="29254-123">Bereitstellen des Zugriffsschlüssels für das Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="29254-123">provide storage account access key</span></span>

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

### <span data-ttu-id="29254-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="29254-124">-StorageAccountType</span></span>
<span data-ttu-id="29254-125">Möglicher Speicher Zugriffstyp GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="29254-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="29254-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29254-126">-Confirm</span></span>
<span data-ttu-id="29254-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29254-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29254-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29254-128">-WhatIf</span></span>
<span data-ttu-id="29254-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29254-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29254-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29254-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29254-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29254-131">CommonParameters</span></span>
<span data-ttu-id="29254-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29254-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29254-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29254-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29254-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29254-134">INPUTS</span></span>

### <span data-ttu-id="29254-135">Keine</span><span class="sxs-lookup"><span data-stu-id="29254-135">None</span></span>

## <span data-ttu-id="29254-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29254-136">OUTPUTS</span></span>

### <span data-ttu-id="29254-137">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="29254-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="29254-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="29254-138">NOTES</span></span>

## <span data-ttu-id="29254-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29254-139">RELATED LINKS</span></span>
