---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006410"
---
# <span data-ttu-id="1069a-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1069a-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="1069a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1069a-102">SYNOPSIS</span></span>
<span data-ttu-id="1069a-103">Erstellt ein neues Speicherkonto in einem Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1069a-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="1069a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1069a-104">SYNTAX</span></span>

### <span data-ttu-id="1069a-105">ParameterSetAffinityGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="1069a-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1069a-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="1069a-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1069a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1069a-107">DESCRIPTION</span></span>
<span data-ttu-id="1069a-108">Das Cmdlet **New-AzureStorageAccount** erstellt ein Konto, das Zugriff auf Azure Storage Services bietet.</span><span class="sxs-lookup"><span data-stu-id="1069a-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="1069a-109">Ein Speicherkonto ist eine weltweit einmalige Ressource im Speichersystem.</span><span class="sxs-lookup"><span data-stu-id="1069a-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="1069a-110">Das Konto ist der übergeordnete Namespace für die BLOB-, Warteschlangen-und Tabellen Dienste.</span><span class="sxs-lookup"><span data-stu-id="1069a-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="1069a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1069a-111">EXAMPLES</span></span>

### <span data-ttu-id="1069a-112">Beispiel 1: Erstellen eines speicherkontos für eine angegebene affinitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="1069a-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="1069a-113">Mit diesem Befehl wird ein Speicherkonto für eine angegebene affinitätsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1069a-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="1069a-114">Beispiel 2: Erstellen eines speicherkontos an einem angegebenen Speicherort</span><span class="sxs-lookup"><span data-stu-id="1069a-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="1069a-115">Mit diesem Befehl wird ein Speicherkonto an einem angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="1069a-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="1069a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="1069a-116">PARAMETERS</span></span>

### <span data-ttu-id="1069a-117">-Affinitygroup</span><span class="sxs-lookup"><span data-stu-id="1069a-117">-AffinityGroup</span></span>
<span data-ttu-id="1069a-118">Gibt den Namen einer vorhandenen affinitätsgruppe im aktuellen Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="1069a-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="1069a-119">Sie können entweder den Parameter *Location* oder *affinitygroup* angeben, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="1069a-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1069a-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1069a-120">-Description</span></span>
<span data-ttu-id="1069a-121">Gibt eine Beschreibung für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="1069a-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="1069a-122">Die Beschreibung kann bis zu 1024 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="1069a-122">The description may be up to 1024 characters in length.</span></span>

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

### <span data-ttu-id="1069a-123">-Information</span><span class="sxs-lookup"><span data-stu-id="1069a-123">-InformationAction</span></span>
<span data-ttu-id="1069a-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1069a-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1069a-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1069a-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1069a-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1069a-126">Continue</span></span>
- <span data-ttu-id="1069a-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1069a-127">Ignore</span></span>
- <span data-ttu-id="1069a-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1069a-128">Inquire</span></span>
- <span data-ttu-id="1069a-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1069a-129">SilentlyContinue</span></span>
- <span data-ttu-id="1069a-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="1069a-130">Stop</span></span>
- <span data-ttu-id="1069a-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1069a-131">Suspend</span></span>

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

### <span data-ttu-id="1069a-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1069a-132">-InformationVariable</span></span>
<span data-ttu-id="1069a-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1069a-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1069a-134">-Label</span><span class="sxs-lookup"><span data-stu-id="1069a-134">-Label</span></span>
<span data-ttu-id="1069a-135">Gibt eine Bezeichnung für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="1069a-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="1069a-136">Die Beschriftung kann bis zu 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="1069a-136">The label may be up to 100 characters in length.</span></span>

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

### <span data-ttu-id="1069a-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="1069a-137">-Location</span></span>
<span data-ttu-id="1069a-138">Gibt den Speicherort des Azure-Datencenters an, in dem das Speicherkonto erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1069a-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="1069a-139">Sie können entweder den Parameter *Location* oder *affinitygroup* , aber nicht beides einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="1069a-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1069a-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="1069a-140">-Profile</span></span>
<span data-ttu-id="1069a-141">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1069a-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1069a-142">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1069a-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1069a-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1069a-143">-StorageAccountName</span></span>
<span data-ttu-id="1069a-144">Gibt einen Namen für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="1069a-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="1069a-145">Der Name des speicherkontos muss für Azure eindeutig sein und muss zwischen 3 und 24 Zeichen lang sein und nur Kleinbuchstaben und Zahlen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1069a-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1069a-146">-Typ</span><span class="sxs-lookup"><span data-stu-id="1069a-146">-Type</span></span>
<span data-ttu-id="1069a-147">Gibt den Typ des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1069a-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="1069a-148">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1069a-148">Valid values are:</span></span>

- <span data-ttu-id="1069a-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="1069a-149">Standard_LRS</span></span>
- <span data-ttu-id="1069a-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="1069a-150">Standard_ZRS</span></span>
- <span data-ttu-id="1069a-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="1069a-151">Standard_GRS</span></span>
- <span data-ttu-id="1069a-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="1069a-152">Standard_RAGRS</span></span>
- <span data-ttu-id="1069a-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="1069a-153">Premium_LRS</span></span>

<span data-ttu-id="1069a-154">Wenn dieser Parameter nicht angegeben wird, lautet der Standardwert Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="1069a-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="1069a-155">Standard_ZRS oder Premium_LRS Konten können nicht in andere Kontotypen geändert werden und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="1069a-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

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

### <span data-ttu-id="1069a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1069a-156">CommonParameters</span></span>
<span data-ttu-id="1069a-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1069a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1069a-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1069a-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1069a-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1069a-159">INPUTS</span></span>

## <span data-ttu-id="1069a-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1069a-160">OUTPUTS</span></span>

## <span data-ttu-id="1069a-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="1069a-161">NOTES</span></span>

## <span data-ttu-id="1069a-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1069a-162">RELATED LINKS</span></span>

[<span data-ttu-id="1069a-163">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1069a-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="1069a-164">Satz-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1069a-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


