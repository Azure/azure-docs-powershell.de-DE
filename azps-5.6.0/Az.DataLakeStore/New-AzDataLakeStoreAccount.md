---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: ee172856bb5935f1a6da4d6dcce92054bd1001e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918944"
---
# <span data-ttu-id="5eca6-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5eca6-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="5eca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eca6-102">SYNOPSIS</span></span>
<span data-ttu-id="5eca6-103">Erstellt ein neues Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="5eca6-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="5eca6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5eca6-104">SYNTAX</span></span>

### <span data-ttu-id="5eca6-105">UserOrSystemAssignedEncryption (Standard)</span><span class="sxs-lookup"><span data-stu-id="5eca6-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eca6-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="5eca6-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eca6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5eca6-107">DESCRIPTION</span></span>
<span data-ttu-id="5eca6-108">Das **Cmdlet New-AzDataLakeStoreAccount** erstellt ein neues Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="5eca6-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="5eca6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5eca6-109">EXAMPLES</span></span>

### <span data-ttu-id="5eca6-110">Beispiel 1: Erstellen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="5eca6-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="5eca6-111">Mit diesem Befehl wird ein Data Lake Store-Konto mit dem Namen ContosoADL für den Ost-US 2-Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="5eca6-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="5eca6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5eca6-112">PARAMETERS</span></span>

### <span data-ttu-id="5eca6-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="5eca6-113">-DefaultGroup</span></span>
<span data-ttu-id="5eca6-114">Gibt die Objekt-ID der AzureActive Directory-Gruppe an, die als Standardgruppenbesitzer für neue Dateien und Ordner verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5eca6-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eca6-115">-DefaultProfile</span></span>
<span data-ttu-id="5eca6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5eca6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5eca6-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="5eca6-117">-DisableEncryption</span></span>
<span data-ttu-id="5eca6-118">Gibt an, dass auf das Konto keine Verschlüsselung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5eca6-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca6-119">-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="5eca6-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca6-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5eca6-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca6-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="5eca6-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca6-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="5eca6-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca6-123">-Location</span><span class="sxs-lookup"><span data-stu-id="5eca6-123">-Location</span></span>
<span data-ttu-id="5eca6-124">Gibt den Speicherort an, der für das Konto verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5eca6-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="5eca6-125">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5eca6-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5eca6-126">Ost-US 2</span><span class="sxs-lookup"><span data-stu-id="5eca6-126">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca6-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5eca6-127">-Name</span></span>
<span data-ttu-id="5eca6-128">Gibt den Namen des zu erstellenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5eca6-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="5eca6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eca6-129">-ResourceGroupName</span></span>
<span data-ttu-id="5eca6-130">Gibt den Namen der Ressourcengruppe an, die das Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="5eca6-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="5eca6-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="5eca6-131">-Tag</span></span>
<span data-ttu-id="5eca6-132">Gibt Tags als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="5eca6-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="5eca6-133">Sie können Tags verwenden, um ein Data Lake Store-Konto aus anderen Azure-Ressourcen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5eca6-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca6-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="5eca6-134">-Tier</span></span>
<span data-ttu-id="5eca6-135">Die gewünschte Verpflichtungsstufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="5eca6-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eca6-136">CommonParameters</span></span>
<span data-ttu-id="5eca6-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eca6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eca6-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eca6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eca6-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5eca6-139">INPUTS</span></span>

### <span data-ttu-id="5eca6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5eca6-140">System.String</span></span>

### <span data-ttu-id="5eca6-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5eca6-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5eca6-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5eca6-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5eca6-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5eca6-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5eca6-144">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5eca6-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="5eca6-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5eca6-145">OUTPUTS</span></span>

### <span data-ttu-id="5eca6-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5eca6-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="5eca6-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5eca6-147">NOTES</span></span>

## <span data-ttu-id="5eca6-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5eca6-148">RELATED LINKS</span></span>

[<span data-ttu-id="5eca6-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5eca6-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5eca6-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5eca6-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5eca6-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5eca6-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5eca6-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5eca6-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


