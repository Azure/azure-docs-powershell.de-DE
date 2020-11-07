---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 5dfe76ad08c59a661d6907c65a53da9397f0a66d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659887"
---
# <span data-ttu-id="4a228-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4a228-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="4a228-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a228-102">SYNOPSIS</span></span>
<span data-ttu-id="4a228-103">Ruft eine Liste der Vaults für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="4a228-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="4a228-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a228-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a228-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a228-105">DESCRIPTION</span></span>
<span data-ttu-id="4a228-106">Das Cmdlet " **Get-AzRecoveryServicesVault** " Ruft eine Liste der Wiederherstellungsdienste-Tresore im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="4a228-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="4a228-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a228-107">EXAMPLES</span></span>

### <span data-ttu-id="4a228-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a228-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="4a228-109">Abrufen der Liste des Tresors im ausgewählten Abonnement</span><span class="sxs-lookup"><span data-stu-id="4a228-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="4a228-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4a228-110">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="4a228-111">Abrufen der Liste des Tresors in der Gruppe "Ressource" im ausgewählten Abonnement</span><span class="sxs-lookup"><span data-stu-id="4a228-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="4a228-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4a228-112">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="4a228-113">Abrufen des Tresors in der Ressourcengruppe mit dem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="4a228-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="4a228-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a228-114">PARAMETERS</span></span>

### <span data-ttu-id="4a228-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a228-115">-DefaultProfile</span></span>
<span data-ttu-id="4a228-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a228-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a228-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4a228-117">-Name</span></span>
<span data-ttu-id="4a228-118">Gibt den Namen des zu abfragenden Tresors an.</span><span class="sxs-lookup"><span data-stu-id="4a228-118">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a228-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a228-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a228-120">Gibt den Namen der Azure-Ressourcengruppe an, in der erstellt werden soll, oder aus der das angegebene Wiederherstellungsdienste-Objekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a228-120">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a228-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a228-121">CommonParameters</span></span>
<span data-ttu-id="4a228-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a228-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a228-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a228-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a228-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a228-124">INPUTS</span></span>

### <span data-ttu-id="4a228-125">Keine</span><span class="sxs-lookup"><span data-stu-id="4a228-125">None</span></span>

## <span data-ttu-id="4a228-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a228-126">OUTPUTS</span></span>

### <span data-ttu-id="4a228-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="4a228-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4a228-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a228-128">NOTES</span></span>

## <span data-ttu-id="4a228-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a228-129">RELATED LINKS</span></span>

[<span data-ttu-id="4a228-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4a228-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="4a228-131">Neu – AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4a228-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="4a228-132">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4a228-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


