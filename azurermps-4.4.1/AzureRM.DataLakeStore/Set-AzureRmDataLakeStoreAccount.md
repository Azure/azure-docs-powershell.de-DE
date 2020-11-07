---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f9ebe1a541baf46e831dbe95b54b2881a03e7454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663588"
---
# <span data-ttu-id="4590b-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4590b-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="4590b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4590b-102">SYNOPSIS</span></span>
<span data-ttu-id="4590b-103">Ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="4590b-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4590b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4590b-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tags] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4590b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4590b-105">DESCRIPTION</span></span>
<span data-ttu-id="4590b-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreAccount** " ändert ein Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="4590b-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="4590b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4590b-107">EXAMPLES</span></span>

### <span data-ttu-id="4590b-108">Beispiel 1: Hinzufügen einer Kategorie zu einem Konto</span><span class="sxs-lookup"><span data-stu-id="4590b-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="4590b-109">Mit diesem Befehl wird das angegebene Tag dem Data Lake Store-Konto mit dem Namen "ContosoADL" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4590b-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="4590b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4590b-110">PARAMETERS</span></span>

### <span data-ttu-id="4590b-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="4590b-111">-AllowAzureIpState</span></span>
<span data-ttu-id="4590b-112">Optional Allow/Block Azure mit Ursprung IPS über die Firewall.</span><span class="sxs-lookup"><span data-stu-id="4590b-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="4590b-113">– Standardgroup</span><span class="sxs-lookup"><span data-stu-id="4590b-113">-DefaultGroup</span></span>
<span data-ttu-id="4590b-114">Gibt die ID einer AzureActive-Verzeichnisgruppe an.</span><span class="sxs-lookup"><span data-stu-id="4590b-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="4590b-115">Diese Gruppe ist die Standardgruppe für Dateien und Ordner, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="4590b-115">This group is the default group for files and folders that you create.</span></span>

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

### <span data-ttu-id="4590b-116">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="4590b-116">-FirewallState</span></span>
<span data-ttu-id="4590b-117">Optional können Sie vorhandene Firewallregeln aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4590b-117">Optionally enable or disable existing firewall rules.</span></span>

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

### <span data-ttu-id="4590b-118">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="4590b-118">-KeyVersion</span></span>
<span data-ttu-id="4590b-119">Wenn der Verschlüsselungstyp vom Benutzer zugewiesen wird, kann der Benutzer seine Schlüssel Version mit diesem Parameter drehen.</span><span class="sxs-lookup"><span data-stu-id="4590b-119">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="4590b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4590b-120">-Name</span></span>
<span data-ttu-id="4590b-121">Gibt den Namen eines Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4590b-121">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="4590b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4590b-122">-ResourceGroupName</span></span>
<span data-ttu-id="4590b-123">Gibt den Namen der Ressourcengruppe an, die das zu ändernde Data Lake Store-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="4590b-123">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="4590b-124">-Tags</span><span class="sxs-lookup"><span data-stu-id="4590b-124">-Tags</span></span>
<span data-ttu-id="4590b-125">Gibt Tags als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="4590b-125">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="4590b-126">Sie können mithilfe von Tags ein Data Lake Store-Konto aus anderen Azure-Ressourcen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4590b-126">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="4590b-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="4590b-127">-Tier</span></span>
<span data-ttu-id="4590b-128">Die gewünschte Verpflichtungs Stufe für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="4590b-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="4590b-129">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="4590b-129">-TrustedIdProviderState</span></span>
<span data-ttu-id="4590b-130">Optional können Sie die vorhandenen vertrauenswürdigen ID-Anbieter aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4590b-130">Optionally enable or disable the existing trusted ID providers.</span></span>

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

### <span data-ttu-id="4590b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4590b-131">-DefaultProfile</span></span>
<span data-ttu-id="4590b-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4590b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4590b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4590b-133">CommonParameters</span></span>
<span data-ttu-id="4590b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4590b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4590b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4590b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4590b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4590b-136">INPUTS</span></span>

## <span data-ttu-id="4590b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4590b-137">OUTPUTS</span></span>

### <span data-ttu-id="4590b-138">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4590b-138">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="4590b-139">Die aktualisierten Kontodetails.</span><span class="sxs-lookup"><span data-stu-id="4590b-139">The updated account details.</span></span>

## <span data-ttu-id="4590b-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="4590b-140">NOTES</span></span>

## <span data-ttu-id="4590b-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4590b-141">RELATED LINKS</span></span>

[<span data-ttu-id="4590b-142">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4590b-142">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4590b-143">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4590b-143">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4590b-144">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4590b-144">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4590b-145">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4590b-145">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


