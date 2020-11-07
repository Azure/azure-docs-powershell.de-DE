---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 0754bd515a846f8524bc7fd9826d36d19d79843a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820155"
---
# <span data-ttu-id="9ed02-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ed02-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="9ed02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ed02-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed02-103">Ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="9ed02-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="9ed02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ed02-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ed02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ed02-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed02-106">Das Cmdlet " **Satz-AzDataLakeStoreAccount** " ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="9ed02-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="9ed02-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ed02-107">EXAMPLES</span></span>

### <span data-ttu-id="9ed02-108">Beispiel 1: Hinzufügen einer Kategorie zu einem Konto</span><span class="sxs-lookup"><span data-stu-id="9ed02-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="9ed02-109">Mit diesem Befehl wird das angegebene Tag dem Data Lake Store-Konto mit dem Namen "ContosoADL" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9ed02-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="9ed02-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ed02-110">PARAMETERS</span></span>

### <span data-ttu-id="9ed02-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="9ed02-111">-AllowAzureIpState</span></span>
<span data-ttu-id="9ed02-112">Optional Allow/Block Azure mit Ursprung IPS über die Firewall.</span><span class="sxs-lookup"><span data-stu-id="9ed02-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="9ed02-113">– Standardgroup</span><span class="sxs-lookup"><span data-stu-id="9ed02-113">-DefaultGroup</span></span>
<span data-ttu-id="9ed02-114">Gibt die ID einer AzureActive-Verzeichnisgruppe an.</span><span class="sxs-lookup"><span data-stu-id="9ed02-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="9ed02-115">Diese Gruppe ist die Standardgruppe für Dateien und Ordner, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="9ed02-115">This group is the default group for files and folders that you create.</span></span>

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

### <span data-ttu-id="9ed02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed02-116">-DefaultProfile</span></span>
<span data-ttu-id="9ed02-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9ed02-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ed02-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="9ed02-118">-FirewallState</span></span>
<span data-ttu-id="9ed02-119">Optional können Sie vorhandene Firewallregeln aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9ed02-119">Optionally enable or disable existing firewall rules.</span></span>

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

### <span data-ttu-id="9ed02-120">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="9ed02-120">-KeyVersion</span></span>
<span data-ttu-id="9ed02-121">Wenn der Verschlüsselungstyp vom Benutzer zugewiesen wird, kann der Benutzer seine Schlüssel Version mit diesem Parameter drehen.</span><span class="sxs-lookup"><span data-stu-id="9ed02-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="9ed02-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9ed02-122">-Name</span></span>
<span data-ttu-id="9ed02-123">Gibt den Namen eines Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9ed02-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="9ed02-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed02-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ed02-125">Gibt den Namen der Ressourcengruppe an, die das zu ändernde Data Lake Store-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="9ed02-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="9ed02-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ed02-126">-Tag</span></span>
<span data-ttu-id="9ed02-127">Gibt Tags als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="9ed02-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="9ed02-128">Sie können mithilfe von Tags ein Data Lake Store-Konto aus anderen Azure-Ressourcen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9ed02-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="9ed02-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="9ed02-129">-Tier</span></span>
<span data-ttu-id="9ed02-130">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="9ed02-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="9ed02-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="9ed02-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="9ed02-132">Optional können Sie die vorhandenen vertrauenswürdigen ID-Anbieter aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9ed02-132">Optionally enable or disable the existing trusted ID providers.</span></span>

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

### <span data-ttu-id="9ed02-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed02-133">CommonParameters</span></span>
<span data-ttu-id="9ed02-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed02-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed02-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed02-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed02-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ed02-136">INPUTS</span></span>

### <span data-ttu-id="9ed02-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed02-137">System.String</span></span>

### <span data-ttu-id="9ed02-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9ed02-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9ed02-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9ed02-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9ed02-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9ed02-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9ed02-141">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. tiertype, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9ed02-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9ed02-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9ed02-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="9ed02-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ed02-143">OUTPUTS</span></span>

### <span data-ttu-id="9ed02-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ed02-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="9ed02-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ed02-145">NOTES</span></span>

## <span data-ttu-id="9ed02-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ed02-146">RELATED LINKS</span></span>

[<span data-ttu-id="9ed02-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ed02-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9ed02-148">Neu – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ed02-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9ed02-149">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ed02-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9ed02-150">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ed02-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


