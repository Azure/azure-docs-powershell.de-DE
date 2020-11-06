---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 22eac04b24e8fec1778578f4e54792b5dcde6d1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504577"
---
# <span data-ttu-id="718fa-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="718fa-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="718fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="718fa-102">SYNOPSIS</span></span>
<span data-ttu-id="718fa-103">Ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="718fa-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="718fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="718fa-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="718fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="718fa-105">DESCRIPTION</span></span>
<span data-ttu-id="718fa-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreAccount** " ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="718fa-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="718fa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="718fa-107">EXAMPLES</span></span>

### <span data-ttu-id="718fa-108">Beispiel 1: Hinzufügen einer Kategorie zu einem Konto</span><span class="sxs-lookup"><span data-stu-id="718fa-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="718fa-109">Mit diesem Befehl wird das angegebene Tag dem Data Lake Store-Konto mit dem Namen "ContosoADL" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="718fa-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="718fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="718fa-110">PARAMETERS</span></span>

### <span data-ttu-id="718fa-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="718fa-111">-AllowAzureIpState</span></span>
<span data-ttu-id="718fa-112">Optional Allow/Block Azure mit Ursprung IPS über die Firewall.</span><span class="sxs-lookup"><span data-stu-id="718fa-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-113">– Standardgroup</span><span class="sxs-lookup"><span data-stu-id="718fa-113">-DefaultGroup</span></span>
<span data-ttu-id="718fa-114">Gibt die ID einer AzureActive-Verzeichnisgruppe an.</span><span class="sxs-lookup"><span data-stu-id="718fa-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="718fa-115">Diese Gruppe ist die Standardgruppe für Dateien und Ordner, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="718fa-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718fa-116">-DefaultProfile</span></span>
<span data-ttu-id="718fa-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="718fa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="718fa-118">-FirewallState</span></span>
<span data-ttu-id="718fa-119">Optional können Sie vorhandene Firewallregeln aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="718fa-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-120">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="718fa-120">-KeyVersion</span></span>
<span data-ttu-id="718fa-121">Wenn der Verschlüsselungstyp vom Benutzer zugewiesen wird, kann der Benutzer seine Schlüssel Version mit diesem Parameter drehen.</span><span class="sxs-lookup"><span data-stu-id="718fa-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="718fa-122">-Name</span></span>
<span data-ttu-id="718fa-123">Gibt den Namen eines Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="718fa-123">Specifies the name of a Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="718fa-125">Gibt den Namen der Ressourcengruppe an, die das zu ändernde Data Lake Store-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="718fa-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="718fa-126">-Tag</span></span>
<span data-ttu-id="718fa-127">Gibt Tags als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="718fa-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="718fa-128">Sie können mithilfe von Tags ein Data Lake Store-Konto aus anderen Azure-Ressourcen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="718fa-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="718fa-129">-Tier</span></span>
<span data-ttu-id="718fa-130">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="718fa-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="718fa-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="718fa-132">Optional können Sie die vorhandenen vertrauenswürdigen ID-Anbieter aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="718fa-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: TrustedIdProviderState
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718fa-133">CommonParameters</span></span>
<span data-ttu-id="718fa-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="718fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718fa-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="718fa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718fa-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="718fa-136">INPUTS</span></span>

### <span data-ttu-id="718fa-137">Keine</span><span class="sxs-lookup"><span data-stu-id="718fa-137">None</span></span>
<span data-ttu-id="718fa-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="718fa-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="718fa-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="718fa-139">OUTPUTS</span></span>

### <span data-ttu-id="718fa-140">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="718fa-140">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="718fa-141">Die aktualisierten Kontodetails.</span><span class="sxs-lookup"><span data-stu-id="718fa-141">The updated account details.</span></span>

## <span data-ttu-id="718fa-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="718fa-142">NOTES</span></span>

## <span data-ttu-id="718fa-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="718fa-143">RELATED LINKS</span></span>

[<span data-ttu-id="718fa-144">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="718fa-144">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="718fa-145">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="718fa-145">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="718fa-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="718fa-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="718fa-147">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="718fa-147">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


