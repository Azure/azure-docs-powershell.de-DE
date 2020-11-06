---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b9154b239e8d4ae2857cba18d3f7dcf9510a62b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477849"
---
# <span data-ttu-id="f3e8e-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f3e8e-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="f3e8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e8e-103">Ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3e8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3e8e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3e8e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3e8e-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e8e-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreAccount** " ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="f3e8e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3e8e-107">EXAMPLES</span></span>

### <span data-ttu-id="f3e8e-108">Beispiel 1: Hinzufügen einer Kategorie zu einem Konto</span><span class="sxs-lookup"><span data-stu-id="f3e8e-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="f3e8e-109">Mit diesem Befehl wird das angegebene Tag dem Data Lake Store-Konto mit dem Namen "ContosoADL" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="f3e8e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3e8e-110">PARAMETERS</span></span>

### <span data-ttu-id="f3e8e-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="f3e8e-111">-AllowAzureIpState</span></span>
<span data-ttu-id="f3e8e-112">Optional Allow/Block Azure mit Ursprung IPS über die Firewall.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="f3e8e-113">– Standardgroup</span><span class="sxs-lookup"><span data-stu-id="f3e8e-113">-DefaultGroup</span></span>
<span data-ttu-id="f3e8e-114">Gibt die ID einer AzureActive-Verzeichnisgruppe an.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="f3e8e-115">Diese Gruppe ist die Standardgruppe für Dateien und Ordner, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-115">This group is the default group for files and folders that you create.</span></span>

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

### <span data-ttu-id="f3e8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e8e-116">-DefaultProfile</span></span>
<span data-ttu-id="f3e8e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3e8e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e8e-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="f3e8e-118">-FirewallState</span></span>
<span data-ttu-id="f3e8e-119">Optional können Sie vorhandene Firewallregeln aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-119">Optionally enable or disable existing firewall rules.</span></span>

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

### <span data-ttu-id="f3e8e-120">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="f3e8e-120">-KeyVersion</span></span>
<span data-ttu-id="f3e8e-121">Wenn der Verschlüsselungstyp vom Benutzer zugewiesen wird, kann der Benutzer seine Schlüssel Version mit diesem Parameter drehen.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="f3e8e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f3e8e-122">-Name</span></span>
<span data-ttu-id="f3e8e-123">Gibt den Namen eines Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="f3e8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3e8e-125">Gibt den Namen der Ressourcengruppe an, die das zu ändernde Data Lake Store-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="f3e8e-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3e8e-126">-Tag</span></span>
<span data-ttu-id="f3e8e-127">Gibt Tags als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="f3e8e-128">Sie können mithilfe von Tags ein Data Lake Store-Konto aus anderen Azure-Ressourcen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e8e-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="f3e8e-129">-Tier</span></span>
<span data-ttu-id="f3e8e-130">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="f3e8e-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="f3e8e-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="f3e8e-132">Optional können Sie die vorhandenen vertrauenswürdigen ID-Anbieter aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-132">Optionally enable or disable the existing trusted ID providers.</span></span>

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

### <span data-ttu-id="f3e8e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e8e-133">CommonParameters</span></span>
<span data-ttu-id="f3e8e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3e8e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e8e-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e8e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e8e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3e8e-136">INPUTS</span></span>

### <span data-ttu-id="f3e8e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f3e8e-137">System.String</span></span>

### <span data-ttu-id="f3e8e-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f3e8e-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f3e8e-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f3e8e-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f3e8e-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f3e8e-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f3e8e-141">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. tiertype, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f3e8e-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f3e8e-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f3e8e-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f3e8e-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3e8e-143">OUTPUTS</span></span>

### <span data-ttu-id="f3e8e-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f3e8e-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="f3e8e-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3e8e-145">NOTES</span></span>

## <span data-ttu-id="f3e8e-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3e8e-146">RELATED LINKS</span></span>

[<span data-ttu-id="f3e8e-147">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f3e8e-147">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f3e8e-148">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f3e8e-148">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f3e8e-149">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f3e8e-149">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f3e8e-150">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f3e8e-150">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


