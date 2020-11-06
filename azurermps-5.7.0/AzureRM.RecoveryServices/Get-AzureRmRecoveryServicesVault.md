---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bbc059751ee4713b59f6b915efe32bdf57419be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501453"
---
# <span data-ttu-id="e5107-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e5107-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="e5107-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5107-102">SYNOPSIS</span></span>
<span data-ttu-id="e5107-103">Ruft eine Liste der Vaults für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="e5107-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5107-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5107-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5107-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5107-105">DESCRIPTION</span></span>
<span data-ttu-id="e5107-106">Das Cmdlet " **Get-AzureRmRecoveryServicesVault** " Ruft eine Liste der Wiederherstellungsdienste-Tresore im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e5107-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="e5107-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5107-107">EXAMPLES</span></span>

### <span data-ttu-id="e5107-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5107-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="e5107-109">Abrufen der Liste des Tresors im ausgewählten Abonnement</span><span class="sxs-lookup"><span data-stu-id="e5107-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="e5107-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5107-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="e5107-111">Abrufen der Liste des Tresors in der Gruppe "Ressource" im ausgewählten Abonnement</span><span class="sxs-lookup"><span data-stu-id="e5107-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="e5107-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e5107-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="e5107-113">Abrufen des Tresors in der Ressourcengruppe mit dem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="e5107-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="e5107-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5107-114">PARAMETERS</span></span>

### <span data-ttu-id="e5107-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e5107-115">-Name</span></span>
<span data-ttu-id="e5107-116">Gibt den Namen des zu abfragenden Tresors an.</span><span class="sxs-lookup"><span data-stu-id="e5107-116">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="e5107-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5107-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5107-118">Gibt den Namen der Azure-Ressourcengruppe an, in der erstellt werden soll, oder aus der das angegebene Wiederherstellungsdienste-Objekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5107-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="e5107-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5107-119">-DefaultProfile</span></span>
<span data-ttu-id="e5107-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5107-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5107-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5107-121">CommonParameters</span></span>
<span data-ttu-id="e5107-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5107-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5107-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5107-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5107-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5107-124">INPUTS</span></span>

### <span data-ttu-id="e5107-125">Keine</span><span class="sxs-lookup"><span data-stu-id="e5107-125">None</span></span>
<span data-ttu-id="e5107-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e5107-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5107-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5107-127">OUTPUTS</span></span>

### <span data-ttu-id="e5107-128">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="e5107-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="e5107-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5107-129">NOTES</span></span>

## <span data-ttu-id="e5107-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5107-130">RELATED LINKS</span></span>

[<span data-ttu-id="e5107-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e5107-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e5107-132">Neu – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e5107-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="e5107-133">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e5107-133">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


