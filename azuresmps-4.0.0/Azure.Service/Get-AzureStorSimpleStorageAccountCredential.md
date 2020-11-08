---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005757"
---
# <span data-ttu-id="bf7c6-101">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bf7c6-101">Get-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="bf7c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf7c6-103">Ruft Anmeldeinformationen für Speicherkonten ab.</span><span class="sxs-lookup"><span data-stu-id="bf7c6-103">Gets credentials for storage accounts.</span></span>

## <span data-ttu-id="bf7c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf7c6-104">SYNTAX</span></span>

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf7c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf7c6-105">DESCRIPTION</span></span>
<span data-ttu-id="bf7c6-106">Das Cmdlet " **Get-AzureStorSimpleStorageAccountCredential** " ruft Anmeldeinformationen für Speicherkonten ab.</span><span class="sxs-lookup"><span data-stu-id="bf7c6-106">The **Get-AzureStorSimpleStorageAccountCredential** cmdlet gets credentials for storage accounts.</span></span>
<span data-ttu-id="bf7c6-107">Dieses Cmdlet ruft alle **StorageAccountCredential** -Objekte ab, die im Dienst konfiguriert sind, oder ein benanntes **StorageAccountCredential**.</span><span class="sxs-lookup"><span data-stu-id="bf7c6-107">This cmdlet gets all **StorageAccountCredential** objects configured in the service or a named **StorageAccountCredential**.</span></span>

## <span data-ttu-id="bf7c6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf7c6-108">EXAMPLES</span></span>

### <span data-ttu-id="bf7c6-109">Beispiel 1: Abrufen aller Anmeldeinformationen für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="bf7c6-109">Example 1: Get all credentials for a resource</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

<span data-ttu-id="bf7c6-110">Dieser Befehl ruft alle verfügbaren Anmeldeinformationen für Speicherkonten für die aktuelle Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="bf7c6-110">This command gets all available credentials for storage accounts for the current resource.</span></span>

### <span data-ttu-id="bf7c6-111">Beispiel 2: Abrufen der Anmeldeinformationen für ein bestimmtes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="bf7c6-111">Example 2: Get the credential for a specific storage account</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

<span data-ttu-id="bf7c6-112">Dieser Befehl ruft die Speicherkonto Anmeldeinformationen für das Speicherkonto mit dem Namen ContosoCloudStorage ab.</span><span class="sxs-lookup"><span data-stu-id="bf7c6-112">This command gets the storage account credential for the storage account named ContosoCloudStorage.</span></span>

## <span data-ttu-id="bf7c6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf7c6-113">PARAMETERS</span></span>

### <span data-ttu-id="bf7c6-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="bf7c6-114">-Profile</span></span>
<span data-ttu-id="bf7c6-115">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="bf7c6-115">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="bf7c6-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bf7c6-116">-StorageAccountName</span></span>
<span data-ttu-id="bf7c6-117">Gibt den Namen des speicherkontos an, für das Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bf7c6-117">Specifies the name of the storage account for which to get credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf7c6-118">CommonParameters</span></span>
<span data-ttu-id="bf7c6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf7c6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf7c6-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf7c6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf7c6-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf7c6-121">INPUTS</span></span>

### <span data-ttu-id="bf7c6-122">Keine</span><span class="sxs-lookup"><span data-stu-id="bf7c6-122">None</span></span>

## <span data-ttu-id="bf7c6-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf7c6-123">OUTPUTS</span></span>

### <span data-ttu-id="bf7c6-124">StorageAccountCredential, IList\<StorageAccountCredential\></span><span class="sxs-lookup"><span data-stu-id="bf7c6-124">StorageAccountCredential, IList\<StorageAccountCredential\></span></span>
<span data-ttu-id="bf7c6-125">Dieses Cmdlet gibt ein **StorageAccountCredential** -Objekt zurück, wenn Sie den *StorageAccountName* -Parameter angeben, oder wenn Sie diesen Parameter nicht angeben, wird **ein \<StorageAccountCredential\> IList** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf7c6-125">This cmdlet returns a **StorageAccountCredential** object, if you specify the *StorageAccountName* parameter, or if you do not specify that parameter, it returns an **IList\<StorageAccountCredential\>** object.</span></span>

## <span data-ttu-id="bf7c6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf7c6-126">NOTES</span></span>

## <span data-ttu-id="bf7c6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf7c6-127">RELATED LINKS</span></span>

[<span data-ttu-id="bf7c6-128">Neu – AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bf7c6-128">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="bf7c6-129">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bf7c6-129">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="bf7c6-130">Satz-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bf7c6-130">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)


