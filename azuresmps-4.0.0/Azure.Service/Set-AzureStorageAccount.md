---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006056"
---
# <span data-ttu-id="22abb-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="22abb-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="22abb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22abb-102">SYNOPSIS</span></span>
<span data-ttu-id="22abb-103">Aktualisiert die Eigenschaften eines speicherkontos in einem Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22abb-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="22abb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22abb-104">SYNTAX</span></span>

### <span data-ttu-id="22abb-105">AccountType (Standard)</span><span class="sxs-lookup"><span data-stu-id="22abb-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22abb-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="22abb-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="22abb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22abb-107">DESCRIPTION</span></span>
<span data-ttu-id="22abb-108">Das Cmdlet " **Satz-AzureStorageAccount** " aktualisiert die Eigenschaften eines Azure Storage-Kontos im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22abb-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="22abb-109">Eigenschaften, die festgesetzt werden können, sind: **Label** , **Description** , **Type** und **GeoReplicationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="22abb-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="22abb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22abb-110">EXAMPLES</span></span>

### <span data-ttu-id="22abb-111">Beispiel 1: Aktualisieren der Bezeichnung für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="22abb-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="22abb-112">Mit diesem Befehl werden die Eigenschaften **Label** und **Description** für das Speicherkonto mit dem Namen ContosoStorage01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="22abb-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="22abb-113">Beispiel 2: Aktivieren der Geo-Replikation für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="22abb-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="22abb-114">Mit diesem Befehl wird die **GeoReplicationEnabled** -Eigenschaft auf $false für das Speicherkonto mit dem Namen ContosoStorage01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22abb-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="22abb-115">Beispiel 3: Deaktivieren der Geo-Replikation für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="22abb-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="22abb-116">Mit diesem Befehl wird die **GeoReplicationEnabled** -Eigenschaft auf $true für das Speicherkonto mit dem Namen ContosoStorage01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22abb-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="22abb-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="22abb-117">PARAMETERS</span></span>

### <span data-ttu-id="22abb-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22abb-118">-Description</span></span>
<span data-ttu-id="22abb-119">Gibt eine Beschreibung für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="22abb-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="22abb-120">Die Beschreibung kann bis zu 1024 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="22abb-120">The description may be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22abb-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="22abb-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="22abb-122">Gibt an, ob das Speicherkonto mit aktivierter Geo-Replikation erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="22abb-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22abb-123">-Information</span><span class="sxs-lookup"><span data-stu-id="22abb-123">-InformationAction</span></span>
<span data-ttu-id="22abb-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="22abb-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="22abb-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="22abb-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22abb-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="22abb-126">Continue</span></span>
- <span data-ttu-id="22abb-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="22abb-127">Ignore</span></span>
- <span data-ttu-id="22abb-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="22abb-128">Inquire</span></span>
- <span data-ttu-id="22abb-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="22abb-129">SilentlyContinue</span></span>
- <span data-ttu-id="22abb-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="22abb-130">Stop</span></span>
- <span data-ttu-id="22abb-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="22abb-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22abb-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="22abb-132">-InformationVariable</span></span>
<span data-ttu-id="22abb-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="22abb-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22abb-134">-Label</span><span class="sxs-lookup"><span data-stu-id="22abb-134">-Label</span></span>
<span data-ttu-id="22abb-135">Gibt eine Bezeichnung für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="22abb-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="22abb-136">Die Beschriftung kann bis zu 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="22abb-136">The label may be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22abb-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="22abb-137">-Profile</span></span>
<span data-ttu-id="22abb-138">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="22abb-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22abb-139">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="22abb-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22abb-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="22abb-140">-StorageAccountName</span></span>
<span data-ttu-id="22abb-141">Gibt den Namen des speicherkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="22abb-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22abb-142">-Typ</span><span class="sxs-lookup"><span data-stu-id="22abb-142">-Type</span></span>
<span data-ttu-id="22abb-143">Gibt den Typ des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="22abb-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="22abb-144">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="22abb-144">Valid values are:</span></span> 

- <span data-ttu-id="22abb-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="22abb-145">Standard_LRS</span></span>
- <span data-ttu-id="22abb-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="22abb-146">Standard_ZRS</span></span>
- <span data-ttu-id="22abb-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="22abb-147">Standard_GRS</span></span>
- <span data-ttu-id="22abb-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="22abb-148">Standard_RAGRS</span></span>
- <span data-ttu-id="22abb-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="22abb-149">Premium_LRS</span></span>

<span data-ttu-id="22abb-150">Wenn dieser Parameter nicht angegeben wird, lautet der Standardwert Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="22abb-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="22abb-151">Der Effekt der Angabe des *GeoReplicationEnabled* -Parameters entspricht dem angeben Standard_GRS im *Type* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="22abb-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="22abb-152">Standard_ZRS oder Premium_LRS Konten können nicht in andere Kontotypen geändert werden und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="22abb-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22abb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22abb-153">CommonParameters</span></span>
<span data-ttu-id="22abb-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22abb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22abb-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22abb-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22abb-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22abb-156">INPUTS</span></span>

## <span data-ttu-id="22abb-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22abb-157">OUTPUTS</span></span>

## <span data-ttu-id="22abb-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="22abb-158">NOTES</span></span>

## <span data-ttu-id="22abb-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22abb-159">RELATED LINKS</span></span>

[<span data-ttu-id="22abb-160">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="22abb-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="22abb-161">Neu – AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="22abb-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="22abb-162">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="22abb-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


