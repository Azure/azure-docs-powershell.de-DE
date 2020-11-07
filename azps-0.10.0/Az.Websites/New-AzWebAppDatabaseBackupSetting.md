---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7ea02fb05c64c751fc339c889098724b2822a8b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842731"
---
# <span data-ttu-id="9d05d-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="9d05d-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="9d05d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d05d-102">SYNOPSIS</span></span>

## <span data-ttu-id="9d05d-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d05d-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d05d-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d05d-104">DESCRIPTION</span></span>
<span data-ttu-id="9d05d-105">Das Cmdlet **New-AzWebAppDatabaseBackupSetting** erstellt eine neue Azure Web App-Sicherungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="9d05d-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="9d05d-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d05d-106">EXAMPLES</span></span>

### <span data-ttu-id="9d05d-107">1:</span><span class="sxs-lookup"><span data-stu-id="9d05d-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="9d05d-108">Erstellt eine Daten Bank Sicherungseinstellung (Verbindungszeichenfolge) vom Typ sqlazure für die angegebene App-ContosoWebApp, die sich in der standardmäßigen Ressourcengruppe-Web-westus befindet.</span><span class="sxs-lookup"><span data-stu-id="9d05d-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9d05d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d05d-109">PARAMETERS</span></span>

### <span data-ttu-id="9d05d-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9d05d-110">-ConnectionString</span></span>
<span data-ttu-id="9d05d-111">Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9d05d-111">Connection String</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d05d-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="9d05d-112">-ConnectionStringName</span></span>
<span data-ttu-id="9d05d-113">Name der Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9d05d-113">Connection String Name</span></span>

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

### <span data-ttu-id="9d05d-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="9d05d-114">-DatabaseType</span></span>
<span data-ttu-id="9d05d-115">Datenbank-Typ (z.b. "sqlazure" oder "MySQL")</span><span class="sxs-lookup"><span data-stu-id="9d05d-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d05d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d05d-116">-DefaultProfile</span></span>
<span data-ttu-id="9d05d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d05d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d05d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9d05d-118">-Name</span></span>
<span data-ttu-id="9d05d-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9d05d-119">WebApp Name</span></span>

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

### <span data-ttu-id="9d05d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d05d-120">CommonParameters</span></span>
<span data-ttu-id="9d05d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d05d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d05d-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d05d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d05d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d05d-123">INPUTS</span></span>

### <span data-ttu-id="9d05d-124">Keine</span><span class="sxs-lookup"><span data-stu-id="9d05d-124">None</span></span>
<span data-ttu-id="9d05d-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9d05d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d05d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d05d-126">OUTPUTS</span></span>

### <span data-ttu-id="9d05d-127">Microsoft. Azure. Management. Websites. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="9d05d-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="9d05d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d05d-128">NOTES</span></span>

## <span data-ttu-id="9d05d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d05d-129">RELATED LINKS</span></span>

