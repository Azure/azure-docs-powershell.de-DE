---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 480532e2fffcc2b03a57c7d0a63cc2737844f652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995435"
---
# <span data-ttu-id="9d079-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="9d079-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="9d079-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d079-102">SYNOPSIS</span></span>

## <span data-ttu-id="9d079-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d079-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d079-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d079-104">DESCRIPTION</span></span>
<span data-ttu-id="9d079-105">Das Cmdlet **New-AzWebAppDatabaseBackupSetting** erstellt eine neue Azure Web App-Sicherungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="9d079-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="9d079-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d079-106">EXAMPLES</span></span>

### <span data-ttu-id="9d079-107">1:</span><span class="sxs-lookup"><span data-stu-id="9d079-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="9d079-108">Erstellt eine Daten Bank Sicherungseinstellung (Verbindungszeichenfolge) vom Typ sqlazure für die angegebene App-ContosoWebApp, die sich in der standardmäßigen Ressourcengruppe-Web-westus befindet.</span><span class="sxs-lookup"><span data-stu-id="9d079-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9d079-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d079-109">PARAMETERS</span></span>

### <span data-ttu-id="9d079-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9d079-110">-ConnectionString</span></span>
<span data-ttu-id="9d079-111">Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9d079-111">Connection String</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d079-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="9d079-112">-ConnectionStringName</span></span>
<span data-ttu-id="9d079-113">Name der Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9d079-113">Connection String Name</span></span>

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

### <span data-ttu-id="9d079-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="9d079-114">-DatabaseType</span></span>
<span data-ttu-id="9d079-115">Datenbank-Typ (z.b. "sqlazure" oder "MySQL")</span><span class="sxs-lookup"><span data-stu-id="9d079-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d079-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d079-116">-DefaultProfile</span></span>
<span data-ttu-id="9d079-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d079-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d079-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9d079-118">-Name</span></span>
<span data-ttu-id="9d079-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9d079-119">WebApp Name</span></span>

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

### <span data-ttu-id="9d079-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d079-120">CommonParameters</span></span>
<span data-ttu-id="9d079-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d079-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d079-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d079-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d079-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d079-123">INPUTS</span></span>

### <span data-ttu-id="9d079-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9d079-124">System.String</span></span>

## <span data-ttu-id="9d079-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d079-125">OUTPUTS</span></span>

### <span data-ttu-id="9d079-126">Microsoft. Azure. Management. Websites. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="9d079-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="9d079-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d079-127">NOTES</span></span>

## <span data-ttu-id="9d079-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d079-128">RELATED LINKS</span></span>
