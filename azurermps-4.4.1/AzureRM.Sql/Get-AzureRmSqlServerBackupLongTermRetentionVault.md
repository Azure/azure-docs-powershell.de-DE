---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 4b63568b4a2bfd6b79c51fcd906819f4831a7ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663813"
---
# <span data-ttu-id="382fd-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="382fd-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="382fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="382fd-102">SYNOPSIS</span></span>
<span data-ttu-id="382fd-103">Ruft einen langfristigen Aufbewahrungs Tresor für Server ab.</span><span class="sxs-lookup"><span data-stu-id="382fd-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="382fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="382fd-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="382fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="382fd-105">DESCRIPTION</span></span>
<span data-ttu-id="382fd-106">Das Cmdlet " **Get-AzureRmSqlServerBackupLongTermRetentionVault** " Ruft das langfristige Aufbewahrungs Depot ab, das auf diesem Server registriert ist.</span><span class="sxs-lookup"><span data-stu-id="382fd-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="382fd-107">Bei Vault handelt es sich um eine Azure-Sicherungs Ressource, die zum Speichern von Sicherungsdaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="382fd-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="382fd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="382fd-108">EXAMPLES</span></span>

## <span data-ttu-id="382fd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="382fd-109">PARAMETERS</span></span>

### <span data-ttu-id="382fd-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="382fd-110">-ResourceGroupName</span></span>
<span data-ttu-id="382fd-111">Gibt den Namen der Ressourcengruppe an, die den Server enthält.</span><span class="sxs-lookup"><span data-stu-id="382fd-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="382fd-112">-Servername</span><span class="sxs-lookup"><span data-stu-id="382fd-112">-ServerName</span></span>
<span data-ttu-id="382fd-113">Gibt den Server an, für den dieses Cmdlet einen Tresor erhält.</span><span class="sxs-lookup"><span data-stu-id="382fd-113">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="382fd-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="382fd-114">-Confirm</span></span>
<span data-ttu-id="382fd-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="382fd-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="382fd-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="382fd-116">-WhatIf</span></span>
<span data-ttu-id="382fd-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="382fd-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="382fd-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="382fd-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="382fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="382fd-119">-DefaultProfile</span></span>
<span data-ttu-id="382fd-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="382fd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="382fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="382fd-121">CommonParameters</span></span>
<span data-ttu-id="382fd-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="382fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="382fd-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="382fd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="382fd-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="382fd-124">INPUTS</span></span>

## <span data-ttu-id="382fd-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="382fd-125">OUTPUTS</span></span>

## <span data-ttu-id="382fd-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="382fd-126">NOTES</span></span>

## <span data-ttu-id="382fd-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="382fd-127">RELATED LINKS</span></span>

[<span data-ttu-id="382fd-128">Satz-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="382fd-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="382fd-129">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="382fd-129">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

