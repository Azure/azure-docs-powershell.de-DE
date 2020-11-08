---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4db6ceb0f806aeffd4dc69580da891de567e4e83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005242"
---
# <span data-ttu-id="e59e2-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e59e2-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="e59e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e59e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e59e2-103">Ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="e59e2-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="e59e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e59e2-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e59e2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e59e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e59e2-106">Das Cmdlet " **Satz-AzDataLakeStoreAccount** " ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="e59e2-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="e59e2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e59e2-107">EXAMPLES</span></span>

### <span data-ttu-id="e59e2-108">Beispiel 1: Hinzufügen einer Kategorie zu einem Konto</span><span class="sxs-lookup"><span data-stu-id="e59e2-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="e59e2-109">Mit diesem Befehl wird das angegebene Tag dem Data Lake Store-Konto mit dem Namen "ContosoADL" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e59e2-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="e59e2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e59e2-110">PARAMETERS</span></span>

### <span data-ttu-id="e59e2-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="e59e2-111">-AllowAzureIpState</span></span>
<span data-ttu-id="e59e2-112">Optional Allow/Block Azure mit Ursprung IPS über die Firewall.</span><span class="sxs-lookup"><span data-stu-id="e59e2-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e2-113">– Standardgroup</span><span class="sxs-lookup"><span data-stu-id="e59e2-113">-DefaultGroup</span></span>
<span data-ttu-id="e59e2-114">Gibt die ID einer AzureActive-Verzeichnisgruppe an.</span><span class="sxs-lookup"><span data-stu-id="e59e2-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="e59e2-115">Diese Gruppe ist die Standardgruppe für Dateien und Ordner, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="e59e2-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59e2-116">-DefaultProfile</span></span>
<span data-ttu-id="e59e2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e59e2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e59e2-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="e59e2-118">-FirewallState</span></span>
<span data-ttu-id="e59e2-119">Optional können Sie vorhandene Firewallregeln aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e59e2-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e2-120">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="e59e2-120">-KeyVersion</span></span>
<span data-ttu-id="e59e2-121">Wenn der Verschlüsselungstyp vom Benutzer zugewiesen wird, kann der Benutzer seine Schlüssel Version mit diesem Parameter drehen.</span><span class="sxs-lookup"><span data-stu-id="e59e2-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e59e2-122">-Name</span></span>
<span data-ttu-id="e59e2-123">Gibt den Namen eines Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e59e2-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="e59e2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e59e2-124">-ResourceGroupName</span></span>
<span data-ttu-id="e59e2-125">Gibt den Namen der Ressourcengruppe an, die das zu ändernde Data Lake Store-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="e59e2-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="e59e2-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="e59e2-126">-Tag</span></span>
<span data-ttu-id="e59e2-127">Gibt Tags als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="e59e2-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="e59e2-128">Sie können mithilfe von Tags ein Data Lake Store-Konto aus anderen Azure-Ressourcen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e59e2-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e2-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="e59e2-129">-Tier</span></span>
<span data-ttu-id="e59e2-130">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="e59e2-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="e59e2-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="e59e2-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="e59e2-132">Optional können Sie die vorhandenen vertrauenswürdigen ID-Anbieter aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e59e2-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59e2-133">CommonParameters</span></span>
<span data-ttu-id="e59e2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e59e2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59e2-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e59e2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59e2-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e59e2-136">INPUTS</span></span>

### <span data-ttu-id="e59e2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e59e2-137">System.String</span></span>

### <span data-ttu-id="e59e2-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e59e2-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e59e2-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e59e2-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e59e2-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e59e2-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e59e2-141">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. tiertype, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e59e2-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e59e2-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e59e2-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e59e2-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e59e2-143">OUTPUTS</span></span>

### <span data-ttu-id="e59e2-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e59e2-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="e59e2-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="e59e2-145">NOTES</span></span>

## <span data-ttu-id="e59e2-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e59e2-146">RELATED LINKS</span></span>

[<span data-ttu-id="e59e2-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e59e2-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e59e2-148">Neu – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e59e2-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e59e2-149">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e59e2-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e59e2-150">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e59e2-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


