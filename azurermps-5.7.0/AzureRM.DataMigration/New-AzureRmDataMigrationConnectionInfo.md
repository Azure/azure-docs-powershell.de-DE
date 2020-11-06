---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479802"
---
# <span data-ttu-id="a32a4-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="a32a4-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="a32a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a32a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a32a4-103">Erstellt ein neues Verbindungs Info Objekt, das den Servertyp und den Namen für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="a32a4-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a32a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a32a4-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="a32a4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a32a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a32a4-106">Das New-AzureRmDataMigrationConnectionInfo-Cmdlet erstellt ein neues Verbindungs Info Objekt, das den Servertyp für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="a32a4-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="a32a4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a32a4-107">EXAMPLES</span></span>

### <span data-ttu-id="a32a4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a32a4-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="a32a4-109">Im vorangehenden Beispiel wird ein neues verbindungsinformationsobjekt erstellt, das SQL als ServerType-Parameter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a32a4-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="a32a4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a32a4-110">PARAMETERS</span></span>

### <span data-ttu-id="a32a4-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a32a4-111">-Confirm</span></span>
<span data-ttu-id="a32a4-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a32a4-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="a32a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32a4-113">-DefaultProfile</span></span>
<span data-ttu-id="a32a4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a32a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a32a4-115">-Servertyp</span><span class="sxs-lookup"><span data-stu-id="a32a4-115">-ServerType</span></span>
<span data-ttu-id="a32a4-116">Enum, die den Servertyp beschreibt, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a32a4-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="a32a4-117">Derzeit unterstützte Werte sind SQL für SQL Server und SQLDB für SQL Azure-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a32a4-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="a32a4-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="a32a4-118">-AuthType</span></span>
<span data-ttu-id="a32a4-119">Der für die Verbindung zu verwendende Authentifizierungstyp.</span><span class="sxs-lookup"><span data-stu-id="a32a4-119">Authentication type to use for connection.</span></span> <span data-ttu-id="a32a4-120">Mögliche Werte sind sqlauthentication und WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="a32a4-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32a4-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="a32a4-121">-DataSource</span></span>
<span data-ttu-id="a32a4-122">Server address\name, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a32a4-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32a4-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="a32a4-123">-TrustServerCertificate</span></span>
<span data-ttu-id="a32a4-124">Boolescher Wert, der angibt, dass die Verschlüsselung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a32a4-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32a4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32a4-125">-WhatIf</span></span>
<span data-ttu-id="a32a4-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a32a4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a32a4-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a32a4-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```





## <span data-ttu-id="a32a4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a32a4-128">INPUTS</span></span>

### <span data-ttu-id="a32a4-129">Keine</span><span class="sxs-lookup"><span data-stu-id="a32a4-129">None</span></span>


## <span data-ttu-id="a32a4-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a32a4-130">OUTPUTS</span></span>

### <span data-ttu-id="a32a4-131">Microsoft. Azure. Management. datamigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="a32a4-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="a32a4-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a32a4-132">NOTES</span></span>

## <span data-ttu-id="a32a4-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a32a4-133">RELATED LINKS</span></span>

