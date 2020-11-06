---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7eea25d4b82dc8a424fea0cbd3e361014c77c396
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500322"
---
# <span data-ttu-id="28a6b-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="28a6b-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="28a6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28a6b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28a6b-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="28a6b-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a6b-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28a6b-104">DESCRIPTION</span></span>
<span data-ttu-id="28a6b-105">Das Cmdlet **New-AzureRmWebAppDatabaseBackupSetting** erstellt eine neue Azure Web App-Sicherungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="28a6b-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="28a6b-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28a6b-106">EXAMPLES</span></span>

### <span data-ttu-id="28a6b-107">1:</span><span class="sxs-lookup"><span data-stu-id="28a6b-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="28a6b-108">Erstellt eine Daten Bank Sicherungseinstellung (Verbindungszeichenfolge) vom Typ sqlazure für die angegebene App-ContosoWebApp, die sich in der standardmäßigen Ressourcengruppe-Web-westus befindet.</span><span class="sxs-lookup"><span data-stu-id="28a6b-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="28a6b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="28a6b-109">PARAMETERS</span></span>

### <span data-ttu-id="28a6b-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="28a6b-110">-ConnectionString</span></span>
<span data-ttu-id="28a6b-111">Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="28a6b-111">Connection String</span></span>

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

### <span data-ttu-id="28a6b-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="28a6b-112">-ConnectionStringName</span></span>
<span data-ttu-id="28a6b-113">Name der Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="28a6b-113">Connection String Name</span></span>

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

### <span data-ttu-id="28a6b-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="28a6b-114">-DatabaseType</span></span>
<span data-ttu-id="28a6b-115">Datenbank-Typ (z.b. "sqlazure" oder "MySQL")</span><span class="sxs-lookup"><span data-stu-id="28a6b-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="28a6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a6b-116">-DefaultProfile</span></span>
<span data-ttu-id="28a6b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28a6b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28a6b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="28a6b-118">-Name</span></span>
<span data-ttu-id="28a6b-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="28a6b-119">WebApp Name</span></span>

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

### <span data-ttu-id="28a6b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a6b-120">CommonParameters</span></span>
<span data-ttu-id="28a6b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a6b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a6b-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28a6b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a6b-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28a6b-123">INPUTS</span></span>

### <span data-ttu-id="28a6b-124">Keine</span><span class="sxs-lookup"><span data-stu-id="28a6b-124">None</span></span>
<span data-ttu-id="28a6b-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="28a6b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28a6b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28a6b-126">OUTPUTS</span></span>

### <span data-ttu-id="28a6b-127">Microsoft. Azure. Management. Websites. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="28a6b-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="28a6b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="28a6b-128">NOTES</span></span>

## <span data-ttu-id="28a6b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28a6b-129">RELATED LINKS</span></span>

