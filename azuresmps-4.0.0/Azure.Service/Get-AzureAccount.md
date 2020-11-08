---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005882"
---
# <span data-ttu-id="13447-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="13447-101">Get-AzureAccount</span></span>

## <span data-ttu-id="13447-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13447-102">SYNOPSIS</span></span>
<span data-ttu-id="13447-103">Ruft Azure-Konten ab, die für Azure PowerShell verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="13447-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="13447-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13447-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13447-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13447-105">DESCRIPTION</span></span>
<span data-ttu-id="13447-106">Das Cmdlet " **Get-AzureAccount** " Ruft die Azure-Konten ab, die für Windows PowerShell verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="13447-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="13447-107">Wenn Sie Ihre Konten für Windows PowerShell verfügbar machen möchten, verwenden Sie die Cmdlets **Add-AzureAccount** oder **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="13447-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="13447-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13447-108">EXAMPLES</span></span>

### <span data-ttu-id="13447-109">Beispiel 1: Abrufen aller Konten</span><span class="sxs-lookup"><span data-stu-id="13447-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="13447-110">Dieser Befehl ruft alle Konten ab, die dem angegebenen Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="13447-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="13447-111">Beispiel 2: Abrufen eines Kontos nach Name</span><span class="sxs-lookup"><span data-stu-id="13447-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="13447-112">Dieser Befehl ruft das ContosoAdmin-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="13447-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="13447-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="13447-113">PARAMETERS</span></span>

### <span data-ttu-id="13447-114">-Name</span><span class="sxs-lookup"><span data-stu-id="13447-114">-Name</span></span>
<span data-ttu-id="13447-115">Ruft nur das angegebene Konto ab.</span><span class="sxs-lookup"><span data-stu-id="13447-115">Gets only the specified account.</span></span>
<span data-ttu-id="13447-116">Der Standardwert ist alle Konten, die für Windows PowerShell verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="13447-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="13447-117">Geben Sie den Kontonamen ein.</span><span class="sxs-lookup"><span data-stu-id="13447-117">Enter the account name.</span></span>
<span data-ttu-id="13447-118">Bei dem Wert für **Name** wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="13447-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="13447-119">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="13447-119">Wildcards are not permitted.</span></span>

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

### <span data-ttu-id="13447-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="13447-120">-Profile</span></span>
<span data-ttu-id="13447-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="13447-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="13447-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="13447-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13447-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13447-123">CommonParameters</span></span>
<span data-ttu-id="13447-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13447-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13447-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13447-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13447-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13447-126">INPUTS</span></span>

### <span data-ttu-id="13447-127">Keine</span><span class="sxs-lookup"><span data-stu-id="13447-127">None</span></span>
<span data-ttu-id="13447-128">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="13447-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="13447-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13447-129">OUTPUTS</span></span>

### <span data-ttu-id="13447-130">Keine</span><span class="sxs-lookup"><span data-stu-id="13447-130">None</span></span>
<span data-ttu-id="13447-131">Dieses Cmdlet gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="13447-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="13447-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="13447-132">NOTES</span></span>

## <span data-ttu-id="13447-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13447-133">RELATED LINKS</span></span>

[<span data-ttu-id="13447-134">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="13447-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="13447-135">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="13447-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="13447-136">Importieren-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="13447-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="13447-137">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="13447-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


